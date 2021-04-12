---
title: Establecimiento del estado del dispositivo en las canalizaciones de la función fija y del sombreador
description: En esta sección se proporcionan las principales diferencias entre establecer el estado del dispositivo con la canalización de sombreador programable y de función fija.
ms.assetid: FF0F2A97-F75A-4AF0-8F5A-EA687523E753
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2d5c0e0ba9e1ac890468654d348b0f8b316f64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274815"
---
# <a name="set-device-state-on-fixed-function-shader-pipelines"></a>Establecimiento del estado del dispositivo en las canalizaciones de la función fija y del sombreador

En esta sección se proporcionan las principales diferencias entre establecer el estado del dispositivo con la canalización de sombreador programable y de función fija.

Estos son los Estados de dispositivo que puede establecer para una canalización de función fija:

-   Transformación e iluminación de funciones fijas [**: IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con \_ D3DRS SHADEMODE, D3DRS SPECULARENABLE \_ , D3DRS \_ Lighting, D3DRS \_ ambiente, D3DRS COLORVERTEX \_ , D3DRS \_ LOCALVIEWER, D3DRS \_ NORMALIZENORMALS, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ SPECULARMATERIALSOURCE, D3DRS AMBIENTMATERIALSOURCE, D3DRS EMISSIVEMATERIALSOURCE, D3DRS VERTEXBLEND, D3DRS INDEXEDVERTEXBLENDENABLE, D3DRS TWEENFACTOR, IDirect3DDevice9:: LightEnable, IDirect3DDevice9:: MultiplyTransform \_ \_ \_ \_ \_ , [**IDirect3DDevice9:: SetFVF**](/windows/desktop/api), [**IDirect3DDevice9:: SetLight**](/windows/desktop/api), [**IDirect3DDevice9::**](/windows/desktop/api)SetMaterial, [](/windows/desktop/api) [](/windows/desktop/api) [](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) IDirect3DDevice9:: SetTransform
-   Sombreador de píxeles de función fija: [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con D3DRS \_ TEXTUREFACTOR, [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
-   Niebla: [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con D3DRS \_ FOGENABLE, D3DRS \_ FOGCOLOR, D3DRS FOGTABLEMODE \_ , D3DRS \_ FOGSTART, D3DRS \_ FOGEND, D3DRS \_ FOGDENSITY, D3DRS \_ RANGEFOGENABLE, D3DRS \_ FOGVERTEXMODE

Estos son los Estados de representación del dispositivo que se pueden establecer con [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) para las canalizaciones de los sombreadores de función fija y programable:

-   Estado de destino de representación: D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2, D3DRS \_ COLORWRITEENABLE3, D3DRS \_ SRGBWRITEENABLE
-   Estado de profundidad: D3DRS \_ ZENABLE, D3DRS \_ ZWRITEENABLE, D3DRS \_ ZFUNC, D3DRS \_ SLOPESCALEDEPTHBIAS, D3DRS \_ DEPTHBIAS
-   Estado de la galería de símbolos: D3DRS \_ STENCILENABLE, D3DRS \_ STENCILFAIL, D3DRS \_ STENCILZFAIL, D3DRS \_ STENCILPASS, D3DRS \_ STENCILFUNC, D3DRS \_ STENCILREF, D3DRS \_ STENCILMASK, D3DRS \_ STENCILWRITEMASK, D3DRS \_ TWOSIDEDSTENCILMODE, D3DRS CCW STENCILFAIL, \_ \_ D3DRS \_ CCW \_ STENCILZFAIL, D3DRS \_ CCW \_ STENCILPASS, D3DRS \_ CCW \_ STENCILFUNC
-   Combinación alfa: D3DRS \_ SRCBLEND, D3DRS \_ DESTBLEND, D3DRS \_ BLENDOP, D3DRS \_ BLENDFACTOR, D3DRS \_ SEPARATEALPHABLENDENABLE, D3DRS \_ SRCBLENDALPHA, D3DRS \_ DESTBLENDALPHA, D3DRS \_ BLENDOPALPHA
-   Prueba alfa: D3DRS \_ ALPHATESTENABLE, D3DRS \_ ALPHAREF, D3DRS \_ ALPHAFUNC
-   Estado de rasterizador: D3DRS \_ FILLMODE, D3DRS \_ LASTPIXEL, D3DRS \_ DITHERENABLE (superficies de 16 bits)
-   Culling: D3DRS \_ CULLMODE
-   Recorte: recorte D3DRS \_ , D3DRS \_ CLIPPLANEENABLE
-   Tijeras: D3DRS \_ SCISSORTESTENABLE
-   Muestras de texturas: D3DRS \_ WRAP0, D3DRS \_ WRAP1, D3DRS \_ WRAP2, D3DRS \_ WRAP3, D3DRS \_ WRAP4, D3DRS \_ WRAP5, D3DRS \_ WRAP6, D3DRS \_ WRAP7, D3DRS \_ WRAP8, D3DRS \_ WRAP9, D3DRS \_ WRAP10, D3DRS \_ WRAP11, D3DRS \_ WRAP12, D3DRS \_ WRAP13, D3DRS \_ WRAP14, D3DRS \_ WRAP15
-   Suavizado de contorno: D3DRS \_ MULTISAMPLEANTIALIAS, D3DRS \_ MULTISAMPLEMASK, D3DRS \_ ANTIALIASEDLINEENABLE
-   Puntos sprites: D3DRS \_ D3DRS, \_ \_ D3DRS min, \_ POINTSPRITEENABLE, D3DRS MAXD3DRS POINTSCALEENABLE \_ \_ \_ , D3DRS \_ POINTSCALE \_ A, D3DRS \_ POINTSCALE \_ B, D3DRS \_ POINTSCALE \_ C
-   N-patches: D3DRS \_ PATCHEDGESTYLE, D3DRS \_ POSITIONDEGREE, D3DRS \_ NORMALDEGREE, D3DRS \_ MINTESSELLATIONLEVEL, D3DRS \_ MAXTESSELLATIONLEVEL, D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ y, D3DRS \_ ADAPTIVETESS \_ Z, D3DRS \_ ADAPTIVETESS \_ W, D3DRS \_ ENABLEADAPTIVETESSELLATION

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas avanzados](advanced-topics.md)
</dt> </dl>

 

 
