# Fortnite-D2-External-Smoothness-Source-Code
This is the Smoothness Source Code I used for d2 Externals. You can use it for anything its just for mouse event.

void smoothing(int smoothing, int delay, int x, int y)
{
  int x_ = 0, y_ = 0, t_ = 0;
  for (int i = 1; i <= smoothing; ++i) {
    int xI = i * x / smoothing;
    int yI = i * y / smoothing;
    int tI = i * delay / smoothing;
    mouse_event(1, xI - x_, yI - y_, 0, 0);
    Sleep(tI - t_);  // Sleep or AccurateSleep
    x_ = xI; y_ = yI; t_ = tI;
  }
}

Discord: https://discord.gg/CBTXrsJsq6
