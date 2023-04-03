# Twitter-Unfollow-App-with-threading

This Python script helps you automate the process of unfollowing users who don't follow you back on Twitter. It uses the Tweepy library to interact with the Twitter API, the `time` module to handle intervals between unfollowing requests, and the `threading` module for parallel execution to improve performance.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [How it Works](#how-it-works)

## Installation

1. Install the required Python libraries:
    `!pip install tweepy==3.9.0`
    `!pip install threaded==4.1.0`

2. Clone this repository to your local machine and navigate to the project directory.

3. Replace the placeholders in the script with your personal Twitter API credentials:
    1. consumer_key = "your_consumer_key"
    2. consumer_secret = "your_consumer_secret"
    3. access_token = "your_access_token"
    4. access_token_secret = "your_access_token_secret"



## Usage

The script will start unfollowing users who don't follow you back and provide status updates in the console.

## How it Works

The script performs the following steps:

1. Authenticate with the Twitter API using the provided credentials.
2. Retrieve the authenticated user's followers and friends (accounts the authenticated user follows).
3. Iterate through the friends list and check if a friend is not a follower.
4. If a friend is not a follower, unfollow the friend using multithreading to improve performance.
5. Wait for a specified interval between unfollowing requests to comply with Twitter API rate limits.

The `process()` function is responsible for executing these steps, while the `get_twitter_api()` function is responsible for handling Twitter API authentication. The `unfollow_friend()` function is used by each thread to unfollow a specific friend if they're not a follower.

Please note that this script is provided for educational purposes only. Be mindful of Twitter's rules and guidelines when using automation. Misuse of this script may result in your account being suspended or banned by Twitter.
