---
description: Una superficie representa un área lineal de memoria de presentación y normalmente reside en la memoria de presentación de la tarjeta de presentación, aunque pueden existir superficies en la memoria del sistema. Las superficies se administran mediante la interfaz IDirect3DSurface9.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Superficies de Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08729cc7252c39ddf71048991a796469f2e8b0b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888593"
---
# <a name="direct3d-surfaces-direct3d-9"></a>Superficies de Direct3D (Direct3D 9)

Una superficie representa un área lineal de memoria de presentación y normalmente reside en la memoria de presentación de la tarjeta de presentación, aunque pueden existir superficies en la memoria del sistema. Las superficies se administran mediante la [**interfaz IDirect3DSurface9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)

-   Búfer de front-in. Rectángulo de memoria que el adaptador de gráficos traduce y muestra en el monitor. En Direct3D, una aplicación nunca escribe directamente en el búfer frontal.
-   Búfer de reserva. Rectángulo de memoria en el que una aplicación puede escribir directamente. El búfer de reserva nunca se muestra directamente en el monitor.
-   Voltear superficies. Proceso de mover el búfer de reserva al búfer principal.
-   Cadena de intercambio. Colección de uno o varios búferes de reserva que se pueden presentar en serie al búfer front-buffer.

## <a name="getting-a-surface"></a>Obtención de una superficie

Cree una superficie mediante una llamada a cualquiera de estos métodos:

-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

Los formatos de superficie determinan cómo se interpretan los datos de cada píxel de la memoria de la superficie. Direct3D usa el [miembro D3DFORMAT](d3dformat.md) de la estructura [**\_ DESC D3DSURFACE**](d3dsurface-desc.md) para describir el formato de superficie. Puede recuperar el formato de una superficie existente llamando al [**método GetDesc.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)

Una vez creada una superficie, puede obtener un puntero a ella llamando a cualquiera de estos métodos:

-   [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [**GetFrontBufferData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [**GetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

La [**interfaz IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) permite acceder indirectamente a la memoria mediante [**el método UpdateSurface.**](/windows/desktop/api) Este método permite copiar una región rectangular de píxeles de una interfaz **IDirect3DSurface9** a otra **interfaz IDirect3DSurface9.** La interfaz de superficie también tiene métodos para acceder directamente a la memoria de presentación. Por ejemplo, puede usar el método [**LockRect**](/windows/desktop/api) para bloquear una región rectangular de memoria para mostrar. Es importante llamar a [**UnlockRect una**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) vez que haya terminado de trabajar con la región rectangular bloqueada en la superficie.

## <a name="additional-surface-topics"></a>Temas adicionales de Surface

Más información sobre cómo usar superficies con cualquiera de estos temas:

-   [Formatos de superficie (Direct3D 9)](surface-formats.md)
-   [¿Qué es una cadena de intercambio? (Direct3D 9)](what-is-a-swap-chain-.md)
-   [Ancho frente a tono (Direct3D 9)](width-vs--pitch.md)
-   [Volteo de superficies (Direct3D 9)](flipping-surfaces.md)
-   [Volteo de página y almacenamiento en búfer hacia atrás (Direct3D 9)](page-flipping-and-back-buffering.md)
-   [Copiar en superficies (Direct3D 9)](copying-to-surfaces.md)
-   [Copiar superficies (Direct3D 9)](copying-surfaces.md)
-   [Acceso directo a la memoria de surface (Direct3D 9)](accessing-surface-memory-directly.md)
-   [Datos de superficie privada (Direct3D 9)](private-surface-data.md)
-   [Controles Gamma (Direct3D 9)](gamma-controls.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 
