---
description: Se puede usar un bloque de estado para capturar solo el estado de píxel (vea State Blocks Save and Restore State (Direct3D 9) (Guardar y restaurar estado de bloques de estado [Direct3D 9]).
ms.assetid: 30624c0a-e30f-4383-bc0c-b43f42403e72
title: Guardar el estado de píxeles con un Bloque de estado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebc7cc408fe919b1569d51f5cdd4e3e5916968d05b90557a17a22377673fdfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797929"
---
# <a name="saving-pixel-state-with-a-stateblock-direct3d-9"></a>Guardar el estado de píxeles con un Bloque de estado (Direct3D 9)

Se puede usar un bloque de estado para capturar solo el estado de píxel (vea State Blocks Save and Restore State (Direct3D 9) [Bloques de estado guardar y restaurar estado [(Direct3D 9)]).](state-blocks-save-and-restore-state.md) El estado siguiente es el estado de píxel:

-   Estado de representación de píxeles (consulte [Canalización de píxeles: estado de representación).](#pixel-pipeline-render-state)
-   Estado de textura de píxeles (consulte [Canalización de píxeles: estado de textura).](#pixel-pipeline-texture-state)
-   Estado del muestreador de píxeles (consulte [Canalización de píxeles: estado del muestreador).](#pixel-pipeline-sampler-state)
-   Sombreador de píxeles actual y cada una de las constantes del sombreador de píxeles.

Para capturar el estado de píxel con un bloque de estado, especifique D3DSBT PIXELSTATE al llamar a \_ [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="pixel-pipeline-render-state"></a>Canalización de píxeles: estado de representación

Los estados de representación del dispositivo afectan al comportamiento de casi todas las partes de la canalización. Los estados de representación se establecen mediante una [**llamada a IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

En la tabla siguiente se incluyen todos los estados de representación que establecen el estado de píxel:



| Representar estados                              | Valor predeterminado      |
|--------------------------------------------|--------------------|
| D3DRS \_ ZENABLE                             | D3D \_ FALSE       |
| D3DRS \_ SPECULARENABLE                      | **FALSE**          |
| [**D3DFILLMODE**](./d3dfillmode.md)   | D3DFILL \_ SOLID     |
| [**D3DSHADEMODE**](./d3dshademode.md) | D3DSHADE \_ GOURAUD  |
| D3DRS \_ ZWRITEENABLE                        | **TRUE**           |
| D3DRS \_ ALPHATESTENABLE                     | **FALSE**          |
| D3DRS \_ LASTPIXEL                           | **TRUE**           |
| D3DRS \_ SRCBLEND                            | D3DBLEND \_ ONE      |
| D3DRS \_ DESTBLEND                           | D3DBLEND \_ ZERO     |
| D3DRSUNC \_                               | D3DCMP \_ LESSEQUAL  |
| D3DRS \_ ALPHAREF                            | 0                  |
| D3DRS \_ ALPHAFUNC                           | D3DCMP \_ ALWAYS     |
| D3DRS \_ DITHERENABLE                        | **FALSE**          |
| D3DRSSTART \_                            | 0                  |
| D3DRSEND \_                              | 1                  |
| \_D3DRSRDDENSITY                          | 1                  |
| D3DRS \_ ALPHABLENDENABLE                    | **FALSE**          |
| D3DRS \_ DEPTHBIAS                           | 0                  |
| D3DRS \_ STENCILENABLE                       | **FALSE**          |
| D3DRS \_ STENCINCIIL                         | D3DSTENCI \_ KEEP |
| D3DRS \_ STENCILZFAIL                        | D3DSTENCI \_ KEEP |
| D3DRS \_ STENCILPASS                         | D3DSTENCI \_ KEEP |
| D3DRS \_ STENCILFUNC                         | D3DCMP \_ ALWAYS     |
| D3DRS \_ STENCILREF                          | 0                  |
| D3DRS \_ STENCILMASK                         | 0xffffffff         |
| D3DRS \_ STENCILWRITEMASK                    | 0xffffffff         |
| D3DRS \_ TEXTUREFACTOR                       | 0xffffffff         |
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
| D3DRS \_ EMISSIVEMATERIALSOURCE              | D3DMCS \_ MATERIAL   |
| D3DRS \_ AMBIENTMATERIALSOURCE               | D3DMCS \_ MATERIAL   |
| D3DRS \_ DIFUSMATERIALSOURCE               | D3DMCS \_ COLOR1     |
| D3DRS \_ SPECULARMATERIALSOURCE              | D3DMCS \_ COLOR2     |
| D3DRS \_ COLORWRITEENABLE                    | 0x0000000f         |
| [**D3DBLENDOP**](./d3dblendop.md)     | D3DBLENDOP \_ ADD    |
| D3DRS \_ DESERCIÓNPRUEBATESTENABLE                   | **FALSE**          |
| D3DRS \_ DESPEDAZCALEDEPTHBIAS                 | 0                  |
| D3DRS \_ ANTIALIASEDLINEENABLE               | **FALSE**          |
| D3DRS \_ TWOSIDEDSTENCILMODE                 | **FALSE**          |
| D3DRS \_ CCW \_ STENCINCINCIIL                    | D3DSTENCI \_ KEEP |
| D3DRS \_ CCW \_ STENCILZFAIL                   | D3DSTENCI \_ KEEP |
| D3DRS \_ CCW \_ STENCILPASS                    | D3DSTENCI \_ KEEP |
| D3DRS \_ CCW \_ STENCILFUNC                    | D3DCMP \_ ALWAYS     |
| D3DRS \_ COLORWRITEENABLE1                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE2                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE3                   | 0x0000000f         |
| D3DRS \_ BLENDFACTOR                         | 0xffffffff         |
| D3DRS \_ SRGBWRITEENABLE                     | 0                  |
| D3DRS \_ SEPARATEALPHABLENDENABLE            | **FALSE**          |
| D3DRS \_ SRCBLEPHA                       | D3DBLEND \_ ONE      |
| D3DRS \_ DESTBLEPHA                      | D3DBLEND \_ ZERO     |
| D3DRS \_ BLENDOPALPHA                        | D3DBLENDOP \_ ADD    |



 

## <a name="pixel-pipeline-sampler-state"></a>Canalización de píxeles: estado del muestreador

Los estados del muestreador controlan los temas relacionados con el muestreo, como el filtrado, el tiling y los modos de dirección de coordenadas de textura. Use [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) para configurar el estado del muestreador (incluido el que se usa en la unidad de teselador para muestrear mapas de desplazamiento). Se ha cambiado el nombre de los estados del muestreador por un prefijo "D3DSAMP" para habilitar la detección de errores en tiempo de compilación al portear \_ desde DirectX 8.

En la tabla siguiente se incluyen todos los estados del muestreador que establecen el estado de píxel:



| Estados del muestreador         | Valor predeterminado     |
|------------------------|-------------------|
| D3DSAMP \_ ADDRESSU      | D3DTADDRESS \_ WRAP |
| D3DSAMP \_ ADDRESSV      | D3DTADDRESS \_ WRAP |
| D3DSAMP \_ ADDRESSW      | D3DTADDRESS \_ WRAP |
| D3DSAMP \_ BORDERCOLOR   | 0x00000000        |
| D3DSAMP \_ MAGFILTER     | D3DTEXF \_ POINT    |
| D3DSAMP \_ MINFILTER     | D3DTEXF \_ POINT    |
| MIPFILTER de D3DSAMP \_     | D3DTEXF \_ NONE     |
| D3DSAMP \_ MIPMAPLODBIAS | 0                 |
| D3DSAMP \_ MAXMIPLEVEL   | 0                 |
| D3DSAMP \_ MAXANISOTROPY | 1                 |
| D3DSAMP \_ SRGBTEXTURE   | 0                 |
| D3DSAMP \_ ELEMENTINDEX  | 0                 |



 

## <a name="pixel-pipeline-texture-state"></a>Canalización de píxeles: estado de textura

Los estados de textura controlan las operaciones de mezcla de textura de la mezcla de varias texturas. Use [**IDirect3DDevice9::SetTextureStageState para**](/windows/desktop/api) configurar los estados de la fase de textura. Use [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para asociar una textura a una fase del muestreador.

En la tabla siguiente se incluyen todos los estados de textura que establecen el estado de píxel:



| Estados de textura                | Valor predeterminado    |
|-------------------------------|------------------|
| COLOROP de D3DTSS \_               | D3DTOP \_ DISABLE  |
| D3DTSS \_ COLORARG1             | TEXTURA \_ D3DTA   |
| D3DTSS \_ COLORARG2             | D3DTA \_ ACTUAL   |
| D3DTSS \_ ALPHAOP               | D3DTOP \_ DISABLE  |
| D3DTSS \_ ALPHAARG1             | TEXTURA \_ D3DTA   |
| D3DTSS \_ ALPHAARG2             | D3DTA \_ ACTUAL   |
| D3DTSS \_ BUMPENVMAT00          | 0                |
| D3DTSS \_ BUMPENVMAT01          | 0                |
| BUMPENVMAT10 de D3DTSS \_          | 0                |
| BUMPENVMAT11 de D3DTSS \_          | 0                |
| D3DTSS \_ TEXCOORDINDEX         | 0                |
| BUMPENVLSCALE DE D3DTSS \_         | 0                |
| BUMPENVLOFFSET DE D3DTSS \_        | 0                |
| TEXTURA DE \_ D3DTSSTRANSFORMFLAGS | D3DTTFF \_ DISABLE |
| D3DTSS \_ COLORARG0             | D3DTA \_ ACTUAL   |
| D3DTSS \_ ALPHAARG0             | D3DTA \_ ACTUAL   |
| D3DTSS \_ RESULTARG             | D3DTA \_ ACTUAL   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[State Blocks Save and Restore State](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
