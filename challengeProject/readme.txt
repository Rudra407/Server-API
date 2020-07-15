Api:
    http://127.0.0.1/upload

        This Api displays a html page with file upload feature.
    
    http://127.0.0.1/uploader

        This Api gets triggered when user clicks upload button and stores files on the server.
        This Api returns the requestId.

    http://127.0.0.1/process?action=<stop|resume|terminate>&requestId=<Enter requestId here obtained>

        This Api when triggered stop or resume or terminate based on action defind in action parameter of the Api.
        returns the action which is performed.

Flow to use the service:

    1) trigger Api -  http://127.0.0.1/upload
    2) upload file and click upload button.
    3) requestId is returned on the webpage.
    4) on the command line each row of file gets printed.
    5) copy the requestId and hit the Api - http://127.0.0.1/process?action=<stop|resume|terminate>&requestId=<Enter requestId here obtained>
    6) based on action, changes get reflected on the commandline i.e, if action is stop, printing on the commandline gets stopped. 
