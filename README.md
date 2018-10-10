# -DLAA-Directionally-Localized-antiAliasing
(DLAA) Directionally Localized antiAliasing 

# Use
* DirectX9
```hlsl 
// Replace 'screen_res' to your screen variable or use default PIXEL_SIZE
#define PIXEL_SIZE screen_res.zw

// Only for DirectX9 Shaders
#define DX9Ver

// Include DLAA
#include "dlaa.h"

float4 main(p_screen I) : COLOR
{
	return DLAAPixelShader(I.tc0);
}
```
* DirectX10 / DirectX11
```hlsl 
// Replace 'screen_res' to your screen variable or use default PIXEL_SIZE
#define PIXEL_SIZE screen_res.zw

// Include DLAA
#include "dlaa.h"

float4 main(p_screen I) : SV_Target
{
	return DLAAPixelShader(I.tc0);
}
```
# Another Settings
* HDR: https://en.wikipedia.org/wiki/Rec._2100
```cpp
#define HDR
```
* Hight passing
```cpp
#define TFU2_HIGH_PASS
```
