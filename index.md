# <center>高考倒计时</center>
## There is ONLY
<center>
<html>
<head>
    <style type="text/css">
        div{
            font-size:20px;
        }
    </style>
    <meta charset="utf-8">
    <meta http-equiv="Content-Type" content="text/html; charset=gb2312" />
    <title>JS时间倒计时</title>
    <script type="text/javascript">
        var time_now_server,time_now_client,time_end,time_server_client;
 
        time_end=new Date("2022/06/18 00:00:0");//结束的时间
        time_end=time_end.getTime();//获取的是毫秒
 
        time_now_server=new Date();//开始的时间
        time_now_server=time_now_server.getTime();
        setTimeout("show_time()",1000);
 
        function show_time()
        {
            var timer = document.getElementById("timer");
            var hourid = document.getElementById("hour");
            if(!timer){
                return ;
            }
            timer.innerHTML =time_now_server;
 
            var time_now,time_distance,str_time;
            var int_day,int_hour,int_minute,int_second,int_millisecond;
            var time_now=new Date();
            time_now=time_now.getTime();
            time_distance=time_end-time_now;
            if(time_distance>0.01)
            {
                int_day=Math.floor(time_distance/8640000000)
                time_distance-=int_day*8640000000;
                int_hour=Math.floor(time_distance/360000000)
                time_distance-=int_hour*360000000;
                int_minute=Math.floor(time_distance/6000000)
                time_distance-=int_minute*6000000;
                int_second=Math.floor(time_distance/100000)
                time_distance-=int_second*100000
                int_millisecond=Math.floor(time_distance/1000)
 
                if(int_hour < 10)
                    int_hour="0"+int_hour;
                if(int_minute<10)
                    int_minute="0"+int_minute;
                if(int_second<10)
                    int_second="0"+int_second;
                if(int_millisecond<100)
                    int_millisecond="0"+int_millisecond
                str_time=int_day+" d "+int_hour+" h "+int_minute+" min "+int_second+" s "+int_millisecond+" ms left";
                timer.innerHTML=str_time;
                setTimeout("show_time()",1000);
            }
            else
            {
                timer.innerHTML =0;
            }
        }
    </script>
</head>
<body>
<div id="timer"></div>
</body>
</html>
</center>
### <center> Before The University/College entrance examination.</center>

