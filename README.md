# GlobalKeyboardHook
this is a global keyboard hook for C# thanks and enjoy

Usage:

using System;
using KeyboardHook;

     private void StartHook()
     {
         _globalKeyboardHook = new GKeyboardHook();
         _globalKeyboardHook.KeyboardPressed += OnKeyPressed;
     }
     
       private void OnKeyPressed(object sender, GlobalKeyboardHookEventArgs e)
        {
            if (e.KeyboardState == GKeyboardHook.KeyboardState.KeyDown)
            {
                Keys loggedKey = e.KeyboardData.Key;

                if (loggedKey == Keys.O)
                {
                   //Do something
                }

                if (loggedKey == Keys.P)
                {
                    //Do something else
                }
            }
        }
        
        public void DisposeHook()
        {
            _globalKeyboardHook?.Dispose();
        }
