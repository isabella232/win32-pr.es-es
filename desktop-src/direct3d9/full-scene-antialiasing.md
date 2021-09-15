---
description: El suavizado de contorno de escena completa hace referencia a desenfocar los bordes de cada polígono de la escena a medida que se rasteriza en un solo paso; no se requiere ningún segundo paso.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Full-Scene suavizado de contorno (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73d559c4b4fec060efbff7468ee29e6c83b64c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127565988"
---
# <a name="full-scene-antialiasing-direct3d-9"></a>Full-Scene suavizado de contorno (Direct3D 9)

El suavizado de contorno de escena completa hace referencia a desenfocar los bordes de cada polígono de la escena a medida que se rasteriza en un solo paso; no se requiere ningún segundo paso. El suavizado de contorno de escena completa, cuando se admite, solo afecta a los triángulos y grupos de triángulos. Las líneas no se pueden suavizar mediante servicios Direct3D. El suavizado de contorno de escena completa se realiza en Direct3D mediante multimuestreo en cada píxel. Cuando se habilita la multimuestreo, todas las submuestras de un píxel se actualizan en un paso, pero cuando se usan para otros efectos que implican varias pasadas de representación, la aplicación puede especificar que solo algunas submuestras se verán afectadas por un paso de representación determinado. Este último enfoque permite la simulación de desenfoque de movimiento, efectos de foco de profundidad de campo, desenfoque de reflexión, entre otros.

En ambos casos, los distintos ejemplos registrados para cada píxel se combinan y se muestran en la pantalla. Esto permite mejorar la calidad de imagen del suavizado de contorno u otros efectos.

Antes de crear un dispositivo con el método [**IDirect3D9::CreateDevice,**](/windows/desktop/api) debe determinar si se admite el suavizado de contorno de escena completa. Para ello, llame al [**método IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) como se muestra en el ejemplo de código siguiente.


```
/*
* The code below assumes that pD3D is a valid pointer 
*   to a IDirect3D9 interface.
*/

if( SUCCEEDED(pD3D->CheckDeviceMultiSampleType( D3DADAPTER_DEFAULT, 
                    D3DDEVTYPE_HAL , D3DFMT_R8G8B8, FALSE, 
                    D3DMULTISAMPLE_2_SAMPLES, NULL ) ) )
// Full-scene antialiasing is supported. Enable it here.
```



El primer parámetro que [**acepta IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) es un número ordinal que denota el adaptador de pantalla que se va a consultar. En este ejemplo se usa D3DADAPTER \_ DEFAULT para especificar el adaptador de pantalla principal. El segundo parámetro es un valor del [**tipo enumerado D3DDEVTYPE,**](./d3ddevtype.md) que especifica el tipo de dispositivo. El tercer parámetro especifica el formato de la superficie. El cuarto parámetro indica a Direct3D si debe preguntar sobre el multimuestreo de ventana completa **(TRUE)** o el suavizado de contorno de escena completa **(FALSE).** En este ejemplo **se usa FALSE** para decir a Direct3D que está inquiriendo sobre el suavizado de contorno de escena completa. El último parámetro especifica la técnica de multimuestreo que desea probar. Use un valor del [**tipo enumerado D3DMULTISAMPLE \_ TYPE.**](./d3dmultisample-type.md) En este ejemplo se comprueba si se admiten dos niveles de multimuestreo.

Si el dispositivo admite el nivel de multimuestreo que desea usar, el siguiente paso es establecer los parámetros de presentación rellenando los miembros adecuados de la estructura DE PARÁMETROS [**D3DPRESENT \_**](d3dpresent-parameters.md) para crear una superficie de representación multimuestreo. Después, puede crear el dispositivo. El código de ejemplo siguiente muestra cómo configurar un dispositivo con una superficie de representación multimuestreo.


```
/*
* The example below assumes that pD3D is a valid pointer 
* to a IDirect3D9 interface, d3dDevice is a pointer to a 
* IDirect3DDevice9 interface, and hWnd is a valid handle
* to a window.
*/

D3DPRESENT_PARAMETER d3dPP
ZeroMemory( &d3dPP, sizeof( d3dPP ) );
d3dPP.Windowed        = FALSE
d3dPP.SwapEffect      = D3DSWAPEFFECT_DISCARD;
d3dPP.MultiSampleType = D3DMULTISAMPLE_2_SAMPLES;
pD3D->CreateDevice(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                    &d3dpp, &d3dDevice)
```



Para usar multimuestreo, el miembro SwapEffect de D3DPRESENT PARAMETER debe establecerse \_ en D3DSWAPEFFECT \_ DISCARD.

El último paso es habilitar el suavizado de contorno multimuestreo llamando al método [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) y estableciendo D3DRS \_ MULTISAMPLEANTIALIAS en **TRUE.** Después de establecer este valor **en TRUE,** cualquier representación que realice tendrá aplicado un multimuestreo. Es posible que quiera habilitar y deshabilitar la multimuestreo, en función de lo que se representa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Antialiasing](antialiasing.md)
</dt> </dl>

 

 
