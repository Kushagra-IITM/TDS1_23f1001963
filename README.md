Creating TDS_1 Project for Tools in Data Science Course

This file will elaborate upon the development of this Project, along with an interesting fact and recommendation for developers based on my analysis.
<br><br>

1] Data Scraping Process

Task Overview

I was assigned the task of scraping GitHub users located in Seattle who have at least 2,000 followers, along with gathering information about their most recent 50 repositories. To achieve this, I utilized the GitHub API, which provides a structured way to access GitHub's vast data.

Detailed Process

Generating a GitHub Token: First, I created a personal access token on GitHub. This token is necessary for authenticating requests to the GitHub API, ensuring I have the appropriate permissions to access user data.

Requesting Data via GitHub API: Using the generated token, I made API requests to search for users based in Seattle who meet the follower threshold. The API endpoint used was specifically tailored to filter users based on location and follower count.
For each user that met the criteria, I then requested their most recent 50 repositories. This involved additional API calls to retrieve repository details, such as names, descriptions, creation dates, and other relevant metadata.

Organizing Data in CSV Format: After gathering the data, I structured it in a CSV format for easy analysis and readability.

Cleaning Up Data: The final step involved cleaning the data to ensure accuracy and consistency. This included ensuring that the repository data was correctly formatted and contained no empty fields.

(
P.S. I know this section was a bit long but it was tough to summarize the entire data scraping phase in just 50 words! I apologize if it felt a bit long, and I hope it didn’t bore you.
)
<br><br>

2] Interesting Fact About the Scraped Data: I found it really interesting that the most followed GitHub user in Seattle has just 12 public repositories while having over 17k followers ! Meanwhile, the users in second and fourth place have 141 and 356 repos, respectively. It seems like having a ton of public repos doesn’t necessarily mean you'll get more followers; it's really about the impact of your work that matters!
<br><br>
3] Actionable recommendation for developers: Since I’m new to data science, I don’t have a lot of pro tips to share yet. But one thing I learned from this project that’s worth mentioning is to always be patient during the data preprocessing stage. It can be really time-consuming and frustrating at times, but it’s important to remember that data science isn’t just about machine learning. Preprocessing is a key part of the process. It might get messy, and you’ll likely need to look things up, but that’s just how it goes!

For example, it took me a bit to figure out why my code was only fetching 50 users. I realized that I needed to use paginated requests because the GitHub API limits how many results you can get in one go. Plus, it helped me avoid hitting those rate limits!
