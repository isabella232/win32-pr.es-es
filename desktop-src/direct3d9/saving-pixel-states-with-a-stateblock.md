---
description: Un bloque de estado se puede usar para capturar solo el estado de píxel (consulte bloques de estado guardar y restaurar estado (Direct3D 9)).
ms.assetid: 30624c0a-e30f-4383-bc0c-b43f42403e72
title: Guardar el estado de los píxeles con un StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80741d9f17939d5795163a3e84c58bcdb9003c70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537942"
---
# <a name="saving-pixel-state-with-a-stateblock-direct3d-9"></a>Guardar el estado de los píxeles con un StateBlock (Direct3D 9)

Un bloque de estado se puede usar para capturar solo el estado de píxel (consulte [bloques de estado guardar y restaurar estado (Direct3D 9)](state-blocks-save-and-restore-state.md)). El estado siguiente es estado de píxel:

-   Estado de representación en píxeles (consulte [canalización de píxeles: estado de representación](#pixel-pipeline-render-state)).
-   Estado de textura en píxeles (consulte [canalización de píxeles: estado de textura](#pixel-pipeline-texture-state)).
-   Estado de muestrario de píxeles (consulte [canalización de píxeles: estado de muestra](#pixel-pipeline-sampler-state)).
-   Sombreador de píxeles actual y cada una de las constantes del sombreador de píxeles.

Para capturar el estado de los píxeles con un bloque de estado, especifique D3DSBT \_ PIXELSTATE cuando llame a [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="pixel-pipeline-render-state"></a>Canalización de píxeles: estado de representación

Los Estados de representación de dispositivos afectan al comportamiento de casi todas las partes de la canalización. Los Estados de representación se establecen mediante una llamada a [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

En la tabla siguiente se incluyen todos los Estados de representación que establecen el estado de los píxeles:



| Estados de representación                              | Valor predeterminado      |
|--------------------------------------------|--------------------|
| D3DRS \_ ZENABLE                             | D3DZB \_ false       |
| D3DRS \_ SPECULARENABLE                      | **FALSE**          |
| [**D3DFILLMODE**](./d3dfillmode.md)   | D3DFILL \_ Solid     |
| [**D3DSHADEMODE**](./d3dshademode.md) | D3DSHADE \_ GOURAUD  |
| D3DRS \_ ZWRITEENABLE                        | **TRUE**           |
| D3DRS \_ ALPHATESTENABLE                     | **FALSE**          |
| D3DRS \_ LASTPIXEL                           | **TRUE**           |
| D3DRS \_ SRCBLEND                            | D3DBLEND \_ uno      |
| D3DRS \_ DESTBLEND                           | D3DBLEND \_ cero     |
| D3DRS \_ ZFUNC                               | D3DCMP \_ LESSEQUAL  |
| D3DRS \_ ALPHAREF                            | 0                  |
| D3DRS \_ ALPHAFUNC                           | D3DCMP \_ siempre     |
| D3DRS \_ DITHERENABLE                        | **FALSE**          |
| D3DRS \_ FOGSTART                            | 0                  |
| D3DRS \_ FOGEND                              | 1                  |
| D3DRS \_ FOGDENSITY                          | 1                  |
| D3DRS \_ ALPHABLENDENABLE                    | **FALSE**          |
| D3DRS \_ DEPTHBIAS                           | 0                  |
| D3DRS \_ STENCILENABLE                       | **FALSE**          |
| D3DRS \_ STENCILFAIL                         | D3DSTENCILOP \_ mantener |
| D3DRS \_ STENCILZFAIL                        | D3DSTENCILOP \_ mantener |
| D3DRS \_ STENCILPASS                         | D3DSTENCILOP \_ mantener |
| D3DRS \_ STENCILFUNC                         | D3DCMP \_ siempre     |
| D3DRS \_ STENCILREF                          | 0                  |
| D3DRS \_ STENCILMASK                         | 0xFFFFFFFF         |
| D3DRS \_ STENCILWRITEMASK                    | 0xFFFFFFFF         |
| D3DRS \_ TEXTUREFACTOR                       | 0xFFFFFFFF         |
| D3DRS \_ WRAP0                               | 0                  |
| D3DRS \_ WRAP1                               | 0                  |
| D3DRS \_ WRAP2                               | 0                  |
| D3DRS \_ WRAP3                               | 0                  |
| D3DRS \_ WRAP4                               | 0                  |
| D3DRS \_ WRAP5                               | 0                  |
| D3DRS \_ WRAP6                               | 0                  |
| D3DRS \_ WRAP7                               | 0                  |
| D3DRS \_ WRAP8                               | 0                  |
| D3DRS \_ WRAP9                               | 0                  |
| D3DRS \_ WRAP10                              | 0                  |
| D3DRS \_ WRAP11                              | 0                  |
| D3DRS \_ WRAP12                              | 0                  |
| D3DRS \_ WRAP13                              | 0                  |
| D3DRS \_ WRAP14                              | 0                  |
| D3DRS \_ WRAP15                              | 0                  |
| D3DRS \_ LOCALVIEWER                         | **TRUE**           |
| D3DRS \_ EMISSIVEMATERIALSOURCE              | \_Material D3DMCS   |
| D3DRS \_ AMBIENTMATERIALSOURCE               | \_Material D3DMCS   |
| D3DRS \_ DIFFUSEMATERIALSOURCE               | D3DMCS \_ COLOR1     |
| D3DRS \_ SPECULARMATERIALSOURCE              | D3DMCS \_ COLOR2     |
| D3DRS \_ COLORWRITEENABLE                    | 0x0000000f         |
| [**D3DBLENDOP**](./d3dblendop.md)     | D3DBLENDOP \_ Agregar    |
| D3DRS \_ SCISSORTESTENABLE                   | **FALSE**          |
| D3DRS \_ SLOPESCALEDEPTHBIAS                 | 0                  |
| D3DRS \_ ANTIALIASEDLINEENABLE               | **FALSE**          |
| D3DRS \_ TWOSIDEDSTENCILMODE                 | **FALSE**          |
| D3DRS \_ CCW \_ STENCILFAIL                    | D3DSTENCILOP \_ mantener |
| D3DRS \_ CCW \_ STENCILZFAIL                   | D3DSTENCILOP \_ mantener |
| D3DRS \_ CCW \_ STENCILPASS                    | D3DSTENCILOP \_ mantener |
| D3DRS \_ CCW \_ STENCILFUNC                    | D3DCMP \_ siempre     |
| D3DRS \_ COLORWRITEENABLE1                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE2                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE3                   | 0x0000000f         |
| D3DRS \_ BLENDFACTOR                         | 0xFFFFFFFF         |
| D3DRS \_ SRGBWRITEENABLE                     | 0                  |
| D3DRS \_ SEPARATEALPHABLENDENABLE            | **FALSE**          |
| D3DRS \_ SRCBLENDALPHA                       | D3DBLEND \_ uno      |
| D3DRS \_ DESTBLENDALPHA                      | D3DBLEND \_ cero     |
| D3DRS \_ BLENDOPALPHA                        | D3DBLENDOP \_ Agregar    |



 

## <a name="pixel-pipeline-sampler-state"></a>Canalización de píxeles: estado de muestra

Los Estados de muestra controlan temas relacionados con el muestreo, como filtrado, mosaico y modos de dirección de coordenadas de textura. Use [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) para configurar el estado de la muestra (incluido el usado en la unidad del teselador para los mapas de desplazamiento de ejemplo). Se ha cambiado el nombre de los Estados de muestra con un \_ prefijo "D3DSAMP" para habilitar la detección de errores en tiempo de compilación al migrar desde DirectX 8.

En la tabla siguiente se incluyen todos los Estados de muestra que establecen el estado de los píxeles:



| Estados de muestra         | Valor predeterminado     |
|------------------------|-------------------|
| D3DSAMP \_ ADDRESSU      | D3DTADDRESS \_ Wrap |
| D3DSAMP \_ ADDRESSV      | D3DTADDRESS \_ Wrap |
| D3DSAMP \_ ADDRESSW      | D3DTADDRESS \_ Wrap |
| D3DSAMP \_ BORDERCOLOR   | 0x00000000        |
| D3DSAMP \_ MAGFILTER     | \_Punto D3DTEXF    |
| D3DSAMP \_ MINFILTER     | \_Punto D3DTEXF    |
| D3DSAMP \_ MIPFILTER     | D3DTEXF \_ ninguno     |
| D3DSAMP \_ MIPMAPLODBIAS | 0                 |
| D3DSAMP \_ MAXMIPLEVEL   | 0                 |
| D3DSAMP \_ MAXANISOTROPY | 1                 |
| D3DSAMP \_ SRGBTEXTURE   | 0                 |
| D3DSAMP \_ ELEMENTINDEX  | 0                 |



 

## <a name="pixel-pipeline-texture-state"></a>Canalización de píxeles: estado de textura

Los Estados de textura controlan las operaciones de combinación de texturas del mezclador de varias texturas. Use [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) para configurar los Estados de la fase de textura. Use [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para asociar una textura a una fase de muestra.

En la tabla siguiente se incluyen todos los Estados de textura que configuran el estado de los píxeles:



| Estados de textura                | Valor predeterminado    |
|-------------------------------|------------------|
| D3DTSS \_ COLOROP               | Deshabilitación de D3DTOP \_  |
| D3DTSS \_ COLORARG1             | \_Textura D3DTA   |
| D3DTSS \_ COLORARG2             | D3DTA \_ actual   |
| D3DTSS \_ ALPHAOP               | Deshabilitación de D3DTOP \_  |
| D3DTSS \_ ALPHAARG1             | \_Textura D3DTA   |
| D3DTSS \_ ALPHAARG2             | D3DTA \_ actual   |
| D3DTSS \_ BUMPENVMAT00          | 0                |
| D3DTSS \_ BUMPENVMAT01          | 0                |
| D3DTSS \_ BUMPENVMAT10          | 0                |
| D3DTSS \_ BUMPENVMAT11          | 0                |
| D3DTSS \_ TEXCOORDINDEX         | 0                |
| D3DTSS \_ BUMPENVLSCALE         | 0                |
| D3DTSS \_ BUMPENVLOFFSET        | 0                |
| D3DTSS \_ TEXTURETRANSFORMFLAGS | Deshabilitación de D3DTTFF \_ |
| D3DTSS \_ COLORARG0             | D3DTA \_ actual   |
| D3DTSS \_ ALPHAARG0             | D3DTA \_ actual   |
| D3DTSS \_ RESULTARG             | D3DTA \_ actual   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estado de guardado y restauración de bloques de estado](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
