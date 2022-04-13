# DLAA: Directionally Localized antiAliasing
DLAA it's fasted aa shader.
2011-2022 (C) 

### Support 
* Dx10
* Dx10.1
* Dx11
* Dx12 

# Use
```hlsl 
// Replace 'screen_res' to your screen size variable

// Include DLAA
#include "dlaa.hlsl"

float4 main(p_screen I) : SV_Target
{
	// Z - Image width | W - Image height
	float2 fSize  = screen_res.zw;
	return DLAAPixelShader(I.tc0, fSize);
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
# Contrib 
* facepuncherfromrussia  
* ForserX
