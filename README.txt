Basic exam app for tw mle (no users)


03/11/2023
    > initial server and client config + CRUD operations
        > mle-basic/client$ ng new client --routing --style=css --minimal
        > mle-basic/client$ ng serve -o 
    > create Angular interface for exams and questions 
        > mle-basic/client$ ng generate interface exam 
            - generates client/src/app/exam.ts
                * can copy over interface from server/src/exam.ts 
    > create service for exams and questions 
        > mle-basic/client$ ng generate service exam 
    > create component (reusable code used to display a view)
        > ng generate component exam-list 
        > ng generate component exam ?? 
        > ng generate component exam-time -m app
    > register copmonent to app.routing.module.ts 
    > TODO: exam-time!!!

03/12/2023
    > exam-options
        - number of questions (range input)
        - show answer details (switch input)
        - "Begin" button
            TODO: > starts test - set timer based on questions, pick specified number of questions, start exam-time!
    TODO: > exam-time form component
        - shows a single question at a time 
         + radio buttons (answer choices)
         + "next" + "previous"
         + list of question numbers (clickable, scrollable)
         + timer
        - hidden answer explanation/details 
    TODO: > exams-list pulls exams out of database, start new test functionality (goto exam-options)

03/14/2023
    > exam-time component~
        - build basic structure
            * Show question # header
            * show single question text 
            * show 4 answer choice radio buttons 
            * Previous and Next buttons 
        - TODO: add functionality to next/previous buttons, pull question info from database 
            > next/prev button should save answer, load next/prev question
                - load saved answer as well in case already answered 
        - TODO: add countdown timer, list of question numbers on the side (ngFor)

    > TODO : don't forget to store answers for current exam !!