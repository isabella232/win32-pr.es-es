---
description: Una superficie representa un área lineal de la memoria de la pantalla y suele residir en la memoria de visualización de la tarjeta de pantalla, aunque pueden existir superficies en la memoria del sistema. La interfaz IDirect3DSurface9 administra las superficies.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Superficies de Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08729cc7252c39ddf71048991a796469f2e8b0b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805198"
---
# <a name="direct3d-surfaces-direct3d-9"></a>Superficies de Direct3D (Direct3D 9)

Una superficie representa un área lineal de la memoria de la pantalla y suele residir en la memoria de visualización de la tarjeta de pantalla, aunque pueden existir superficies en la memoria del sistema. La interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) administra las superficies.

-   Búfer frontal. Un rectángulo de memoria que el adaptador de gráficos traduce y que se muestra en el monitor. En Direct3D, una aplicación nunca escribe directamente en el búfer frontal.
-   Búfer de reserva. Un rectángulo de memoria en el que puede escribir una aplicación directamente. El búfer de reserva nunca se muestra directamente en el monitor.
-   Voltear superficies. Proceso de mover el búfer de reserva al búfer frontal.
-   Cadena de intercambio. Colección de uno o más búferes de reserva que se pueden presentar en serie al búfer frontal.

## <a name="getting-a-surface"></a>Obtención de una superficie

Cree una superficie llamando a cualquiera de estos métodos:

-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

Los formatos de superficie determinan cómo se interpretan los datos de cada píxel en la memoria de la superficie. Direct3D usa el miembro [D3DFORMAT](d3dformat.md) de la [**estructura \_ DESC de D3DSURFACE**](d3dsurface-desc.md) para describir el formato de la superficie. Puede recuperar el formato de una superficie existente llamando al método [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) .

Una vez creada una superficie, puede obtener un puntero llamando a cualquiera de estos métodos:

-   [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [**GetFrontBufferData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [**GetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

La interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) permite el acceso indirecto a la memoria a través del método [**UpdateSurface**](/windows/desktop/api) . Este método permite copiar una región rectangular de píxeles de una interfaz **IDirect3DSurface9** a otra interfaz **IDirect3DSurface9** . La interfaz Surface también tiene métodos para acceder directamente a la memoria de la pantalla. Por ejemplo, puede usar el método [**LockRect**](/windows/desktop/api) para bloquear una región rectangular de la memoria de la pantalla. Es importante llamar a [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) después de haber terminado de trabajar con la región rectangular bloqueada en la superficie.

## <a name="additional-surface-topics"></a>Temas de superficie adicionales

Obtenga más información sobre cómo usar las superficies con cualquiera de estos temas:

-   [Formatos de superficie (Direct3D 9)](surface-formats.md)
-   [¿Qué es una cadena de intercambio? (Direct3D 9)](what-is-a-swap-chain-.md)
-   [Ancho frente a paso (Direct3D 9)](width-vs--pitch.md)
-   [Voltear superficies (Direct3D 9)](flipping-surfaces.md)
-   [Intercambio de páginas y almacenamiento en búfer de retroceso (Direct3D 9)](page-flipping-and-back-buffering.md)
-   [Copiar en superficies (Direct3D 9)](copying-to-surfaces.md)
-   [Copiar superficies (Direct3D 9)](copying-surfaces.md)
-   [Acceso directo a la memoria de la superficie (Direct3D 9)](accessing-surface-memory-directly.md)
-   [Datos de la superficie privada (Direct3D 9)](private-surface-data.md)
-   [Controles gamma (Direct3D 9)](gamma-controls.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 
