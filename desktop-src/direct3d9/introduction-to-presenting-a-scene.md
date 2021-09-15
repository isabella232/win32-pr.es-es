---
description: Las API de presentación son un conjunto de métodos que controlan el estado del dispositivo que afecta a lo que el usuario ve en el monitor. Estos métodos incluyen la configuración de modos de presentación y métodos una vez por fotograma que se usan para presentar imágenes al usuario.
ms.assetid: fb2ddc0d-50ac-48aa-8a5c-f232b0f8e7aa
title: Introducción a la presentación de una escena (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d909f2d7fcc04cd58c27c7598ca8f826b27f48a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574072"
---
# <a name="introduction-to-presenting-a-scene-direct3d-9"></a>Introducción a la presentación de una escena (Direct3D 9)

Las API de presentación son un conjunto de métodos que controlan el estado del dispositivo que afecta a lo que el usuario ve en el monitor. Estos métodos incluyen la configuración de modos de presentación y métodos una vez por fotograma que se usan para presentar imágenes al usuario.

-   [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
-   [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
-   [**IDirect3DDevice9::GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
-   [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
-   [**IDirect3DDevice9::GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)

Es necesario estar familiarizado con los términos siguientes para comprender las API de presentación.

-   búfer front.buffer. Rectángulo de memoria que el adaptador de gráficos traduce y se muestra en el monitor u otro dispositivo de salida.
-   búfer de reserva. Superficie cuyo contenido se puede promover al búfer frontal.
-   cadena de intercambio. Colección de búferes de reserva que se pueden presentar en serie al búfer front-buffer. Normalmente, una cadena de intercambio de pantalla completa presenta imágenes posteriores con la interfaz de controlador de dispositivo (DDI) de volteo, y una cadena de intercambio por ventanas presenta imágenes con el DDI de borrado.

Dado que Direct3D 9 tiene una cadena de intercambio como propiedad del dispositivo, siempre hay al menos una cadena de intercambio por dispositivo. La [**interfaz IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) tiene un conjunto de métodos que manipulan la cadena de intercambio implícita y son una copia de la propia interfaz de la cadena de intercambio. Las aplicaciones pueden crear cadenas de intercambio adicionales; sin embargo, esto no es necesario para la aplicación típica de una sola ventana o de pantalla completa.

El búfer frontal no se expone directamente en Direct3D 9. Como resultado, las aplicaciones no pueden bloquear ni representar en el búfer frontal. Para obtener más información, vea [Acceso al búfer frontal de color (Direct3D 9).](accessing-the-color-front-buffer.md)

> [!Note]  
> DirectX 7 proporcionó varias API de presentación que se han llamado juntas. Un buen ejemplo de esto es la secuencia IDirectDraw7::SetCooperativeLevel, IDirectDraw7::SetDisplayMode e IDirectDraw7::CreateSurface. Además, los métodos IDirectDrawSurface7::Flip e IDirectDrawSurface7::Blt señalaron el transporte de fotogramas representados al monitor. Direct3D 9 contrae estos grupos de API en dos métodos principales, Reset y Present. Restablezca las subsumes SetCooperativeLevel, SetDisplayMode, CreateSurface y algunos de los parámetros que se invertirán. Presentar subsumes voltear y los usos de presentación de blit.

 

Una llamada a [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) representa un restablecimiento implícito del dispositivo. La API de Direct3D 9 no tiene ninguna noción de superficie principal; no se puede crear un objeto que represente la superficie principal. Se considera una propiedad interna del dispositivo.

Las rampas Gamma están asociadas a una cadena de intercambio y se manipulan con los métodos [**IDirect3DDevice9::GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) [**e IDirect3DDevice9::SetGammaRamp.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Presentación de una escena](presenting-a-scene.md)
</dt> </dl>

 

 
