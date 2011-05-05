Background process
===================

This will allow the email-sending process to happen in the background,
working around php's time limit. Without this process, sending emails
to a large email list is not possible.

Demands (required)
----------

-	Stability. It should be able to run for hours and days alike. This
	also means high cpu usage it not allowed - it could result in an
	unstable server
- 	Reliability. The background process should work on as many systems
	as possible. This includes safemode, installations that do not allow
	system calls, non-adjustable time limits, etc.
-	Cron-able. Because it might be needed to start the process on a later
	date, it should be possible to start the process using cron.
-	Intervention-able. This is related to the cron-ability; it should be
	possible to start, stop, pause and resume a process using an API.
	
Wishes (optional)
-------

-	Reusability. The ability to run a process in the background can be
	used by more applications than only the EN. If it is possible to
	make this background process reusable, it would be a big plus.
-	Extendable. There are a number of techniques that allow a process
	to run in the background. Because all of these techniques have their
	pros and cons, it would be nice if it was possible to implement
	multiple methods and choosing the right method for the job.