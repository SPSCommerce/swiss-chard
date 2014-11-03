Chard - redis backed scheduler for celery

To configure, set CELERYBEAT_SCHEDULER to chard.scheduler.ChardScheduler and specify a CELERY_REDIS_SCHEDULER_URL.
```
    CELERYBEAT_SCHEDULER="chard.scheduler.ChardScheduler",
    CELERY_REDIS_SCHEDULER_URL="redis://",
```

nosetests -v --cover-package=chard --with-cover -s

Tests require redis running locally and will use the db 0. It spins up celery and tests to make sure the correct number of taks are scheduled.  Could probably be explanded more and get coverage of some of the edge cases.

