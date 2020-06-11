# OneByteWallhack
CS:GO wallhack достигается патчем одного байта в игре. Написан скрипт на Python 3.

Оно делает тоже самое что команда **r_drawothermodels 2**, но не трогая квары (cvar).

## Как оно работает
Эта программа патчит ассемблерный код, созданный путем компиляции [следующей строки игрового кода](https://github.com/ValveSoftware/source-sdk-2013/blob/0d8dceea4310fde5706b3ce1c70609d72a38efdf/mp/src/game/client/c_baseanimating.cpp#L3149):
```cpp
int extraFlags = 0;
if ( r_drawothermodels.GetInt() == 2 )
{	
    extraFlags |= STUDIO_WIREFRAME;	
}
```
 ## Зависимость
**pymem==1.0**

