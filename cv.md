# [CV]()
# Nikita Kutas
## Trainee Front-end Web Developer
### **My contact information:**
+ **Location:** Minsk, Belarus
+ **Phone number:** +375-29-349-64-58
+ **Email:** mikitakutas@gmail.com
+ **GitHub:** [MikitaKutas](https://github.com/MikitaKutas)
### About me:
From early childhood, computers and their workings have captivated me. Over the years, after the advent of the internet, I gradually delved into this complex world of computers. Eventually, I came to the decision that I want to intertwine my life with this field.

I graduated from Minsk State Energy College and then got a job as a locksmith for control and measuring devices and automation. I've been working in this field for two and a half years. However, I don't want to continue in this direction, so a year after starting work, I enrolled in the Belarusian State University in the part-time program at the Faculty of Mechanics and Mathematics. At the same time, I started learning JavaScript and Front-end development. After a while, I decided to learn C# and a bit of ASP.NET, but after a year, I realized that I enjoy Front-end much more. Now, I plan to complete the RS School course and find a job as a Front-end developer.

Following my college graduation and a few months spent at my initial job, I firmly resolved to shift my career path to programming. This decision was bolstered by my attempts to learn Frontend development since college days. With this background, I am primarily focusing on Frontend, though I am also delving into Backend, particularly learning ASP.NET, for a more holistic understanding and general development.
### Skills and proficiency:
+ HTML 5, CSS 3, Sass
+ JavaScript fundamentals
+ C# fundamentals
+ Git, GitHub, GitLab
+ VS, VS Code, Rider, WebStorm
+ Figma basics
### Code example:
This is my solution to the task from LeetCode written in C#
```
public class Solution {
    public int Jump(int[] nums)
    {
        var n = nums.Length;

        if (n == 1)
            return 0;

        var jumps = new int[n];

        for (var i = n - 2; i >= 0; i--)
        {
            if (nums[i] == 0)
                jumps[i] = int.MaxValue - 1;
            else if (nums[i] >= n - i - 1)
                jumps[i] = 1;
            else
            {
                var minJump = int.MaxValue - 1;
                for (var j = i + 1; j < n && j <= i + nums[i]; j++)
                {
                    minJump = Math.Min(minJump, jumps[j] + 1);
                }

                jumps[i] = minJump;
            }
        }

        return jumps[0];
    }
}