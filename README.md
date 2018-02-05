# C-Project
void Game::UpdateModel()
{
	if (wnd.kbd.KeyIsPressed(VK_RIGHT))
	{
		if (inhibitRight)
		{
		}
		else
		{
			vx = vx + 1;
			inhibitRight = true;

		}
	}
	else
	{
		inhibitRight = false;
	}
	if (wnd.kbd.KeyIsPressed(VK_LEFT))
	{
		if (inhibitLeft)
		{
		}
		else
		{
			vx = vx - 1;
			inhibitLeft = true;
		}

	}
	else
	{
		inhibitLeft = false;
	}
	if (wnd.kbd.KeyIsPressed(VK_UP))
	{
		if (inhibitUp)
		{
		}
		else
		{
			vy = vy + 1;
			inhibitUp = true;
		}
	}
	else
	{
		inhibitUp = false;
	}
	if (wnd.kbd.KeyIsPressed(VK_DOWN))
	{
		if (inhibitDown)
		{
		}
		else
		{
			vy = vy - 1;
			inhibitDown = true;
		}
	}
	else
	{
		inhibitDown = false;
	}
	x = x + vx;
		y = y + vy;
		 
	
	if (wnd.kbd.KeyIsPressed(VK_CONTROL))
	{
		gb = 0;
	}
	shapeIsChanged = wnd.kbd.KeyIsPressed(VK_SHIFT);
}

void Game::ComposeFrame()
{
	
	


	if (shapeIsChanged)
	{
		gfx.PutPixel(x - 5,y - 5, 255, gb, gb);
		gfx.PutPixel(x - 5,y - 4, 255, gb, gb);
		gfx.PutPixel(x - 5,y - 3, 255, gb, gb);
		gfx.PutPixel(x - 4,y - 5, 255, gb, gb);
		gfx.PutPixel(x - 3,y - 5, 255, gb, gb);
		gfx.PutPixel(x - 5,y + 5, 255, gb, gb);
		gfx.PutPixel(x - 5,y + 4, 255, gb, gb);
		gfx.PutPixel(x - 5,y + 3, 255, gb, gb);
		gfx.PutPixel(x - 4,y + 5, 255, gb, gb);
		gfx.PutPixel(x - 3,y + 5, 255, gb, gb);
		gfx.PutPixel(x + 5,y - 5, 255, gb, gb);
		gfx.PutPixel(x + 5,y - 4, 255, gb, gb);
		gfx.PutPixel(x + 5,y - 3, 255, gb, gb);
		gfx.PutPixel(x + 4,y - 5, 255, gb, gb);
		gfx.PutPixel(x + 3,y - 5, 255, gb, gb);
		gfx.PutPixel(x + 5,y + 5, 255, gb, gb);
		gfx.PutPixel(x + 5,y + 4, 255, gb, gb);
		gfx.PutPixel(x + 5,y + 3, 255, gb, gb);
		gfx.PutPixel(x + 4,y + 5, 255, gb, gb);
		gfx.PutPixel(x + 3,y + 5, 255, gb, gb);
	}				 	   
	else			 	   
	{				 	   
		gfx.PutPixel(x - 5,y, 255, gb, gb);
		gfx.PutPixel(x - 4,y, 255, gb, gb);
		gfx.PutPixel(x - 3,y, 255, gb, gb);
		gfx.PutPixel(x + 3,y, 255, gb, gb);
		gfx.PutPixel(x + 4,y, 255, gb, gb);
		gfx.PutPixel(x + 5,y, 255, gb, gb);
		gfx.PutPixel(x, y - 5, 255, gb, gb);
		gfx.PutPixel(x, y - 4, 255, gb, gb);
		gfx.PutPixel(x, y - 3, 255, gb, gb);
		gfx.PutPixel(x, y + 3, 255, gb, gb);
		gfx.PutPixel(x, y + 4, 255, gb, gb);
		gfx.PutPixel(x, y + 5, 255, gb, gb);
	}
}
