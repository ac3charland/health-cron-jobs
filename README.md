# Health Cron Jobs

## Rationale

Research shows that sitting and staring at a screen for long periods of uninterrupted time is bad for your health. While these behaviors are unavoidable for most office workers, standing hourly and looking away from a screen every 20 minutes mitigates the health risk. The problem is: who is going to remember to look away from their screen every 20 minutes?

I created this repo to address this problem for myself at my workplace. It contains instructions and scripts to send alerts (on Mac) that remind the user to stand hourly and look away from their screen every 20 minutes. 

## `crontab` Setup

1. Run `crontab -e` in Terminal to edit your machine's cron jobs.
2. Add the following lines:
```
0 * * * * [path to repo]/health-cron-jobs/stand.sh
20,40 * * * * [path to repo]/health-cron-jobs/look-away.sh
```

The first line runs a script that sends an hourly reminder to stand. The second runs a script that sends a reminder 20 and 40 minutes after the hour to look away from the screen.

Change the path for each script to the path on your machine (ex. ~/path/to/this/repo/health-cron-jobs/stand.sh)
