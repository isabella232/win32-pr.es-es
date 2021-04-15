---
description: El suavizado de contorno completo de la escena se refiere al desenfoque de los bordes de cada polígono de la escena a medida que se rasteriza en un solo paso; no se requiere ningún segundo paso.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Suavizado de contorno Full-Scene (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73d559c4b4fec060efbff7468ee29e6c83b64c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536837"
---
# <a name="full-scene-antialiasing-direct3d-9"></a>Suavizado de contorno Full-Scene (Direct3D 9)

El suavizado de contorno completo de la escena se refiere al desenfoque de los bordes de cada polígono de la escena a medida que se rasteriza en un solo paso; no se requiere ningún segundo paso. El suavizado de contorno completo de la escena, cuando se admite, solo afecta a los triángulos y grupos de triángulos. Las líneas no se pueden alisar con los servicios Direct3D. El suavizado de contorno completo de la escena se realiza en Direct3D mediante el muestreo múltiple en cada píxel. Cuando se habilita el muestreo múltiple, todas las submuestras de un píxel se actualizan en un solo paso, pero cuando se usan para otros efectos que implican varias fases de representación, la aplicación puede especificar que solo se verán afectadas por un paso de representación determinado. Este último enfoque permite la simulación del desenfoque de movimiento, los efectos de enfoque de profundidad de campo, el desenfoque de reflexión, etc.

En ambos casos, los distintos ejemplos registrados para cada píxel se combinan y se envían a la pantalla. Esto permite mejorar la calidad de la imagen del suavizado de contorno u otros efectos.

Antes de crear un dispositivo con el método [**IDirect3D9:: CreateDevice**](/windows/desktop/api) , debe determinar si se admite el suavizado de contorno completo de la escena. Para ello, llame al método [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) tal y como se muestra en el ejemplo de código siguiente.


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



El primer parámetro que [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) acepta es un número ordinal que denota el adaptador de pantalla que se va a consultar. En este ejemplo \_ se usa el valor predeterminado de D3DADAPTER para especificar el adaptador de pantalla principal. El segundo parámetro es un valor del tipo enumerado [**D3DDEVTYPE**](./d3ddevtype.md) , que especifica el tipo de dispositivo. El tercer parámetro especifica el formato de la superficie. El cuarto parámetro indica a Direct3D si se debe consultar sobre el suavizado de contorno completo (**true**) de la ventana completa o el suavizado de contorno de la escena completa (**false**). En este ejemplo se usa **false** para indicar a Direct3D que está consultando el suavizado de contorno completo de la escena. El último parámetro especifica la técnica de muestreo múltiple que desea probar. Use un valor del tipo enumerado [**D3DMULTISAMPLE \_ Type**](./d3dmultisample-type.md) . Este ejemplo prueba para ver si se admiten dos niveles de muestreo múltiple.

Si el dispositivo admite el nivel de muestreo múltiple que quiere usar, el siguiente paso es establecer los parámetros de presentación rellenando los miembros adecuados de la estructura de [**\_ parámetros D3DPRESENT**](d3dpresent-parameters.md) para crear una superficie de representación de ejemplo múltiple. Después, puede crear el dispositivo. En el código de ejemplo siguiente se muestra cómo configurar un dispositivo con una superficie de representación de muestreo múltiple.


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



Para usar el muestreo múltiple, el miembro SwapEffect del \_ parámetro D3DPRESENT debe establecerse en D3DSWAPEFFECT \_ discard.

El último paso es habilitar el suavizado de contorno múltiple llamando al método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) y establecer el valor de D3DRS \_ MULTISAMPLEANTIALIAS en **true**. Después de establecer este valor en **true**, cualquier representación que realice tendrá aplicado un muestreo múltiple. Puede habilitar y deshabilitar el muestreo múltiple, en función de lo que esté representando.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suavizado](antialiasing.md)
</dt> </dl>

 

 
