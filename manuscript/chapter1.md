# Ops Readiness Checklist  
+ Backup up employee laptops. Recommend crashplan
+ Anti-theft for employee laptops, Recommend Prey
+ Using Enterprise password manager and don’t allow people to use the same password for multiple accounts.
+ A staging environment to test changes before they go live.
+ Searchable logs stored off the server. You need something like logentries or papertrail to store your web logs for a longer period of time.
+ Tracking exceptions.
+ Sending transactional email. Recommend Mandrill.
+ Database Restore Testing. Notice how I didn't say backups? You need to regularly test that you can restore your database(s) for use with in a different deployment. I recommend doing a database restore from production into staging regularly, so that you know it works. You will be surprised at how many things break the first time you try to do this, and will sleep better when you know that your restore/recovery process is regularly being exercised.
+ User behavior monitoring. Is anyone using your site? What pages are popular? Recommend segment.io
+ Performance monitoring. Recommend Pingdom to monitor average site load speed. NewRelic to guide developers working on speeding up the app.
+ Availability monitoring. Recommend pingdom
+ Communicating with customers in case of an outage - statuspage.io, hosted separately from your app
+ Security vulnerability patching: database, web server, application code, linux server. Schedule!
+ Redundant storage of uploaded files (separate from code and database). S3 etc.
+ SSL. Serve everything over SSL. Don't let your certificates expire (set reminders or wire certificate checks into your monitoring system. Make sure your staging systems use SSL also.
+ User Feedback. If you really want to engage your customers, give them a way to talk back to you. If you want to send your customers email, why wouldn't you also give them an easy way to send you a comment or question? Customer.io is a great tool for this.
+ DNS. Is your DNS secured with MFA, or is it vulnerable to the first person who can hack your email? Can you track changes made to DNS records over time so that you can revert an incorrect change?

{width=20%,float=right}
!(images/logo.png)