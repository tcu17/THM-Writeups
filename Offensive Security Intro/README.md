# Offensive Security Intro
## Thomas Urbain - April 3, 2025

![image](https://github.com/user-attachments/assets/16263614-5277-4d69-91e1-f9afe044fabd)

### Overview
In this room, we will learn the following:
- What is Offensive Security and what does it entail?
- How to learn more about Offensive Security
- Beginner web hacking techniques
- Ways to exploit vulnerabilities in web applications
- Basic Linux terminal commands used in Offensive Security
- Different careers in Offensive Security

In this room we will use the following tools:
- Gobuster
-- Command line tool to enumerate subdirectories in web servers

### Task 1 - What is Offensive Security?

"To outsmart a hacker, you need to think like one."

This is the core of "Offensive Security." It involves breaking into computer systems, exploiting software bugs, and finding loopholes in applications to gain unauthorized access. The goal is to understand hacker tactics and enhance our system defences.

#### Beginning Your Learning Journey

In this TryHackMe room, you will be guided through hacking your first website in a legal and safe environment. The goal is to show you how an ethical hacker operates.

But before we do that, let's review by answering the questions below. Type your answer in the text box after the question and click the "Submit" button. When you're done, proceed to Task 2.

###### Question 1:
![image](https://github.com/user-attachments/assets/49046bbb-df89-4e9b-bb94-0d9efe3d0284)

###### Answer:
![image](https://github.com/user-attachments/assets/c04d465f-d7ab-46da-9248-0fd5e8152c60)
Reasoning:
In the above section, it explains offensive security using examples such as breaking into computer systems, exploiting software bugs, and finding loopholes in applications to gain unauthorized access.
Defensive security would be the opposite of this, attempting to thwart the plans of those in offensive security, preventing them attacking with the above methods.

### Task 2 - Hacking your first machine
Here at TryHackMe, we use Virtual Machines to create simulated environments that serve as practical complements to rooms. 

In this room, we have prepared a fake bank application called Fakebank that you can safely hack. To start this machine, click on the Start Machine button below.

Start Machine

Your screen should be split in half, showing this content on the left and the newly launched machine on the right. If you hide it later, you can always click on the Show Split View button at the top to display it again. You should see a browser window showing the website below:

![image](https://github.com/user-attachments/assets/6a9d4de1-5bdc-4cc6-8b8e-00d1c57174cd)

If you don't see the one shown above, use the "Show Split View" button at the top of this page.

#### Your First Hack

We will use a command-line application called "Gobuster" to brute-force FakeBank's website to find hidden directories and pages. Gobuster will take a list of potential page or directory names and try accessing a website with each of them; if the page exists, it tells you.

##### Step 1. Open A Terminal

A terminal, also known as the command line, allows us to interact with a computer without using a graphical user interface. On the machine, open the terminal by clicking on the Terminal icon on the right of the screen.

![image](https://github.com/user-attachments/assets/08dcd0a7-150a-445f-a346-189c2a9a654b)

##### Step 2. Use Gobuster To Find Hidden Website Pages

Most companies have an admin portal page, giving their staff access to basic admin controls for day-to-day operations. For a bank, an employee might need to transfer money to and from client accounts. Due to human error or negligence, there may be instances when these pages are not made private, allowing attackers to find hidden pages that show or give access to admin controls or sensitive data.

To begin, type the following command into the terminal to find potentially hidden pages on FakeBank's website using Gobuster (a command-line security application).

<i>gobuster -u http://fakebank.thm -w wordlist.txt dir</i>

The command will run and show you an output similar to this:

![image](https://github.com/user-attachments/assets/c3d65951-e466-446b-8b2b-b189de462e65)

In the command above, <i>-u</i> is used to state the website we're scanning, <i>-w</i> takes a list of words to iterate through to find hidden pages.

You will see that Gobuster scans the website with each word in the list, finding pages that exist on the site. Gobuster will have told you the pages in the list of page/directory names (indicated by Status: 200).

![image](https://github.com/user-attachments/assets/c1ddecd8-e688-4437-8fd2-28b090bcd960)

##### Step 3. Hack The Bank

You should have found a secret bank transfer page that allows you to transfer money between bank accounts (<i>/bank-transfer</i>). Type the hidden page into the FakeBank website using the browser's address bar.

![image](https://github.com/user-attachments/assets/359f0d90-3b3f-488f-9a30-d0a3a3b15d6e)

From this page, an attacker has authorized access and can steal money from any bank account. As an ethical hacker, you would (with permission) find vulnerabilities in their application and report them to the bank to fix them before a hacker exploits them.

Your mission is to transfer $2000 from bank account 2276 to your account (account number 8881). If your transfer was successful, you should now be able to see your new balance reflected on your account page.

Go there now and confirm you got the money! (You may need to hit Refresh for the changes to appear)

###### Question 2
![image](https://github.com/user-attachments/assets/39c9c38e-d623-4252-8be4-f8bf144ec6e0)

###### Answer:
First, we must enumerate the subdirectories using Gobuster.
![image](https://github.com/user-attachments/assets/bf5b5b9a-8380-4101-9785-7f0f667a48c5)

As seen in the image above, we are given two subdirectories to try.
The first of which is /images.
![image](https://github.com/user-attachments/assets/78255c24-cda0-4dee-b418-5ff5dbafc853)

As we can see, the /images subdirectory does not seem to be what we are looking for.
After trying /bank-transfer, we are greeted with the following webpage.
![image](https://github.com/user-attachments/assets/774b9d0c-6d44-4523-863d-6236583cd2b6)

This looks like the correct page!
If we recall, we were tasked with sending $2000 from 2276 to 8881, which we can easily do on this page.
![image](https://github.com/user-attachments/assets/9964b86e-da25-460a-bfb8-d53cb87c81b9)

After pressing "Send," we are redirected to the page shown below.
![image](https://github.com/user-attachments/assets/994e8214-4959-48da-891c-8d05489a47b2)

We are then tasked with returning to our account page, which we can do by clicking on the Fake Bank logo on the top left.
After returning, we are greeted with a banner stating that we have successfully hacked the bank, and our answer, <i>BANK-HACKED</i>.
![image](https://github.com/user-attachments/assets/9f493c86-6df3-487d-9d99-76ee0f1746ae)

We can enter this into the answer field on TryHackMe.
![image](https://github.com/user-attachments/assets/88c024a5-2ffe-4a64-b41b-ab111a9b7242)

###### Question 3
![image](https://github.com/user-attachments/assets/9877b701-cc3f-4bfd-9b6a-42d9b99ffee7)

###### Answer:
No answer is needed. This is simply a field for you to reflect on what you have done in this task.

###### Question 4
![image](https://github.com/user-attachments/assets/f7b5319f-e55d-4184-a6b2-913253161ab8)
No answer is needed. Simply terminate the machine using the "Terminate" button near the top of the page.
![image](https://github.com/user-attachments/assets/c9fcc67c-1ebb-402f-bfed-d690e4d8ad6a)

### Task 3 - Careers in cyber security

#### How can I start learning?

People often wonder how others become hackers (security consultants) or defenders (security analysts fighting cybercrime), and the answer is simple. Break it down, learn an area of cyber security you're interested in, and regularly practice using hands-on exercises. Build a habit of learning a little bit each day on TryHackMe, and you'll acquire the knowledge to get your first job in the industry.

Trust us; you can do it! Just take a look at some people who have used TryHackMe to get their first security job:

- Paul went from a construction worker to a security engineer. <a href="https://tryhackme.com/r/resources/blog/construction-worker-to-security-engineer-how-paul-used-tryhackme-to-land-his-first-job-in-security">Read more</a>
- Kassandra went from a music teacher to a security professional. <a href="https://tryhackme.com/r/resources/blog/the-teacher-becomes-the-student">Read more</a>
- Brandon used TryHackMe while at school to get his first job in cyber. <a href="https://tryhackme.com/r/resources/blog/brandons-success-story">Read more</a>

#### What careers are there?

The cyber careers room goes into more depth about the different careers in cyber. However, here is a short description of a few offensive security roles:
  - Penetration Tester - Responsible for testing technology products for finding exploitable security vulnerabilities.
  - Red Teamer - Plays the role of an adversary, attacking an organization and providing feedback from an enemy's perspective.
  - Security Engineer - Design, monitor, and maintain security controls, networks, and systems to help prevent cyberattacks.

###### Question 5
![image](https://github.com/user-attachments/assets/6b3bd0ef-a344-474a-a13d-e95688185a20)

###### Answer:
No answer is needed. You have successfully completed the room!

### Reflection

In this room, we learned the basics of what offensive security entails.

We learned how to use Gobuster in the Linux terminal for subdirectory enumeration, as well as how to exploit vulnerabilities we found along the way.
Remember that we may only exploit vulnerabilities we have written permission for! Exploiting vulnerabilities without written permission is illegal.

This room also showed us how we must think as a member of defensive security. Allowing people to transfer money from accounts that they do not own damages the integrity part of the CIA Triad.
Those transferring money should only be able to transfer it out of their account, and they must also be authenticated to send funds from a given account.

Congratulations for completing this room! Keep progressing through the vast world of cyber security!
