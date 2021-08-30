---
description: Un bloque de estado se puede usar para capturar solo el estado de vértice (vea State Blocks Save and Restore State (Direct3D 9) [Guardar y restaurar estado de bloques de estado (Direct3D 9)]).
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: Guardar estados de vértice con un Bloque de estado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f3ebef7bda74e30d84ff193a80df6bc6ce7eae83a648f9b7e1d05b89bdb269
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026115"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a>Guardar estados de vértice con un Bloque de estado (Direct3D 9)

Se puede usar un bloque de estado para capturar solo el estado de vértice (vea State Blocks Save and Restore State (Direct3D 9) [Guardar y restaurar estado [(Direct3D 9)].](state-blocks-save-and-restore-state.md) El estado siguiente es estado de vértice:

-   Estado de representación de vértices (vea [Canalización de vértices: estado de representación).](#vertex-pipeline-render-state)
-   Estado del muestreador de vértices (consulte [Canalización de vértices: estado del muestreador).](#vertex-pipeline-sampler-state)
-   Estado de textura de vértice (vea [Canalización de vértices: estado de textura).](#vertex-pipeline-texture-state)
-   Segmentos de modo NPatch de [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).
-   Cada luz de [**IDirect3DDevice9::SetLight**](/windows/desktop/api), así como si la luz está habilitada o no con [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).
-   Sombreador de vértices actual y cada una de las constantes del sombreador de vértices.
-   Para cada secuencia de vértices, almacene el valor del divisor [**de IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   Declaración de vértice actual.

Para capturar el estado de vértice con un bloque de estado, especifique D3DSBT VERTEXSTATE al llamar a \_ [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="vertex-pipeline-render-state"></a>Canalización de vértices: Estado de representación

Los estados de representación del dispositivo afectan al comportamiento de casi todas las partes de la canalización. Los estados de representación se establecen mediante una [**llamada a IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

En la tabla siguiente se incluyen todos los estados de representación que establecen el estado del vértice:



| Representar estados                           | Valor predeterminado          |
|-----------------------------------------|------------------------|
| D3DRS \_ CULLMODE                         | D3DCULL \_ CCW           |
| D3DRSCOLOR \_                         | 0                      |
| D3DRS \_ CONFIGURABLEMODE                     | D3DFOG \_ NONE           |
| D3DRSSTART \_                         | 0                      |
| D3DRSEND \_                           | 1                      |
| \_D3DRSRDDENSITY                       | 1                      |
| D3DRS \_ RANGEFOGENABLE                   | **FALSE**              |
| D3DRS \_ AMBIENT                          | 0                      |
| D3DRS \_ COLORVERTEX                      | **TRUE**               |
| \_D3DRSVERTEXMODE                    | D3DFOG \_ NONE           |
| RECORTE DE \_ D3DRS                         | **TRUE**               |
| ILUMINACIÓN D3DRS \_                         | **TRUE**               |
| D3DRS \_ LOCALVIEWER                      | **TRUE**               |
| D3DRS \_ EMISSIVEMATERIALSOURCE           | D3DMCS \_ MATERIAL       |
| D3DRS \_ AMBIENTMATERIALSOURCE            | D3DMCS \_ MATERIAL       |
| D3DRS \_ DIFFUSEMATERIALSOURCE            | D3DMCS \_ COLOR1         |
| D3DRS \_ SPECULARMATERIALSOURCE           | D3DMCS \_ COLOR2         |
| D3DRS \_ VERTEXBLEND                      | D3DVBF \_ DISABLE        |
| CLIPPLANEENABLE DE D3DRS \_                  | 0                      |
| D3DRS \_ POINTSIZE                        | Dependiente del controlador       |
| D3DRS \_ APUNTA A \_ MIN                   | 1                      |
| PUNTOS \_ D3DRSPRITEENABLE                | **FALSE**              |
| D3DRS \_ POINTSCALEENABLE                 | **FALSE**              |
| D3DRS \_ POINTSCALE \_ A                    | 1                      |
| D3DRS \_ POINTSCALE \_ B                    | 0                      |
| D3DRS \_ POINTSCALE \_ C                    | 0                      |
| D3DRS \_ MULTISAMPLEANTIALIAS             | **TRUE**               |
| D3DRS \_ MULTISAMPLEMASK                  | 0xffffffff             |
| D3DRS \_ PATCHEDGESTYLE                   | D3DPATCHEDGE \_ DISCRETE |
| D3DRS \_ POINTSIZE \_ MAX                   | 1                      |
| D3DRS \_ INDEXEDVERTEXBLENDENABLE         | **FALSE**              |
| D3DRS \_ TWEENFACTOR                      | 0                      |
| D3DRS \_ POSITIONDEGREE                   | D3DDEGREE \_ CUBIC       |
| D3DRS \_ NORMALDEGREE                     | D3DDEGREE \_ LINEAR      |
| D3DRS \_ MINTESSELLATIONLEVEL             | 1                      |
| D3DRS \_ MAXTESSELLATIONLEVEL             | 1                      |
| D3DRS \_ ADAPTIVETESS \_ X                  | 0                      |
| D3DRS \_ ADAPTIVETESS \_ Y                  | 0                      |
| D3DRS \_ ADAPTIVETESS \_ Z                  | 1                      |
| D3DRS \_ ADAPTIVETESS \_ W                  | 0                      |
| D3DRS \_ ENABLEADAPTIVETESSELLATION"/> | **FALSE**              |



 

## <a name="vertex-pipeline-sampler-state"></a>Canalización de vértices: estado del muestreador

Los estados del muestreador controlan los temas relacionados con el muestreo, como el filtrado, el tiling y los modos de dirección de coordenadas de textura. Use [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) para configurar el estado del muestreador (incluido el que se usa en la unidad de teselador para muestrear mapas de desplazamiento). Se ha cambiado el nombre de los estados del muestreador por un prefijo "D3DSAMP" para habilitar la detección de errores en tiempo de compilación al porte desde \_ DirectX 8.

En la tabla siguiente se incluyen todos los estados del muestreador que establecen el estado del vértice:



| Estados del muestreador      | Valor predeterminado |
|---------------------|---------------|
| D3DSAMP \_ DMAPOFFSET | 256           |



 

## <a name="vertex-pipeline-texture-state"></a>Canalización de vértices: estado de textura

Los estados de textura controlan las operaciones de mezcla de textura del combinador de varias texturas. Use [**IDirect3DDevice9::SetTextureStageState para**](/windows/desktop/api) configurar los estados de textura. Use [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para asociar una textura a una fase de sampler.

En la tabla siguiente se incluyen todos los estados de textura que establecen el estado del vértice:



| Estados de textura                | Valor predeterminado    |
|-------------------------------|------------------|
| D3DTSS \_ TEXCOORDINDEX         | 0                |
| TEXTURA DE \_ D3DTSSTRANSFORMFLAGS | D3DTTFF \_ DISABLE |



 

D3DTSS \_ TEXCOORDINDEX es un estado de procesamiento de vértices de función fija. Si se usa un sombreador de vértices programable, se omite este estado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estado: Guardar y restaurar estado de bloques de estado](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
