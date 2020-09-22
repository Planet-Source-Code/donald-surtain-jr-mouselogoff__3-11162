<div align="center">

## MouseLogoff


</div>

### Description

This program simulates a person moving the mouse,clicking the start button and then logging then off. I made this program because i am very lazy!!!!!lol

I know there are faster ways to logoff such as:

ExitWindows(0,0);

system("shutdown -l");

system("rundll32 user32.dll,ExitWindowsEx");

But I wanted to do it in a different way.

Please vote!!!!!
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Donald Surtain Jr\.](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/donald-surtain-jr.md)
**Level**          |Advanced
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |C\+\+ \(general\), Microsoft Visual C\+\+, Borland C\+\+
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__3-1.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/donald-surtain-jr-mouselogoff__3-11162/archive/master.zip)

### API Declarations

```
#include &lt;windows.h&gt;
```


### Source Code

```
#include <windows.h>
int main(int argc,char*argv[])
{
  HWND hwnd = FindWindow(NULL,argv[0]);
  ShowWindow(hwnd,SW_HIDE);
  int x = 350;
  int y = 150;
   for(x>60;y<580;y++)
   {
   SetCursorPos(x,y);
   Sleep(1);
     if(x!=60)
     {
      --x;
     }
   }
  Sleep(500);
  mouse_event(MOUSEEVENTF_LEFTDOWN,x,y,0,0);
  Sleep(500);
  mouse_event(MOUSEEVENTF_LEFTUP,x,y,0,0);
  for(y>550;x==60;y--)
  {
   SetCursorPos(x,y);
   Sleep(1);
   if(y==550)
   {
   break;
   }
  }
  for(x<200;y==550;x++)
   {
   SetCursorPos(x,y);
   Sleep(1);
   if(x==200)
   {
   break;
   }
  }
   keybd_event(VkKeyScan('l'),0,0,0);
   Sleep(1000);
   keybd_event(VkKeyScan('l'),0,0,0);
   return 0;
}
```

