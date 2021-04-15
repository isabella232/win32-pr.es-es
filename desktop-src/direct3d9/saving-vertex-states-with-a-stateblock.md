---
description: Un bloque de estado se puede usar para capturar solo el estado del vértice (vea bloques de estado guardar y restaurar estado (Direct3D 9)).
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: Guardar Estados de vértice con un StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c6bc7fd291a2609ef60709f05a04fe8d27f8eb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696093"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a>Guardar Estados de vértice con un StateBlock (Direct3D 9)

Un bloque de estado se puede usar para capturar solo el estado del vértice (vea [bloques de estado guardar y restaurar estado (Direct3D 9)](state-blocks-save-and-restore-state.md)). El estado siguiente es el estado del vértice:

-   Estado de representación de vértices (vea [canalización de vértices: estado de representación](#vertex-pipeline-render-state)).
-   Estado del muestrario de vértices (consulte [canalización de vértices: estado de muestra](#vertex-pipeline-sampler-state)).
-   Estado de textura de vértices (vea [canalización de vértices: estado de textura](#vertex-pipeline-texture-state)).
-   Los segmentos del modo NPatch de [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).
-   Cada luz de [**IDirect3DDevice9:: SetLight**](/windows/desktop/api), así como si la luz está habilitada o no con [**IDirect3DDevice9:: LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).
-   Sombreador de vértices actual y cada una de las constantes de sombreador de vértices.
-   Para cada flujo de vértices, almacene el valor de divisor de [**IDirect3DDevice9:: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   La declaración de vértice actual.

Para capturar el estado del vértice con un bloque de estado, especifique D3DSBT \_ VERTEXSTATE cuando llame a [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="vertex-pipeline-render-state"></a>Canalización de vértices: estado de representación

Los Estados de representación de dispositivos afectan al comportamiento de casi todas las partes de la canalización. Los Estados de representación se establecen mediante una llamada a [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

En la tabla siguiente se incluyen todos los Estados de representación que establecen el estado del vértice:



| Estados de representación                           | Valor predeterminado          |
|-----------------------------------------|------------------------|
| D3DRS \_ CULLMODE                         | D3DCULL \_ CCW           |
| D3DRS \_ FOGCOLOR                         | 0                      |
| D3DRS \_ FOGTABLEMODE                     | D3DFOG \_ ninguno           |
| D3DRS \_ FOGSTART                         | 0                      |
| D3DRS \_ FOGEND                           | 1                      |
| D3DRS \_ FOGDENSITY                       | 1                      |
| D3DRS \_ RANGEFOGENABLE                   | **FALSE**              |
| \_Ambiente D3DRS                          | 0                      |
| D3DRS \_ COLORVERTEX                      | **TRUE**               |
| D3DRS \_ FOGVERTEXMODE                    | D3DFOG \_ ninguno           |
| Recorte de D3DRS \_                         | **TRUE**               |
| \_Iluminación D3DRS                         | **TRUE**               |
| D3DRS \_ LOCALVIEWER                      | **TRUE**               |
| D3DRS \_ EMISSIVEMATERIALSOURCE           | \_Material D3DMCS       |
| D3DRS \_ AMBIENTMATERIALSOURCE            | \_Material D3DMCS       |
| D3DRS \_ DIFFUSEMATERIALSOURCE            | D3DMCS \_ COLOR1         |
| D3DRS \_ SPECULARMATERIALSOURCE           | D3DMCS \_ COLOR2         |
| D3DRS \_ VERTEXBLEND                      | Deshabilitación de D3DVBF \_        |
| D3DRS \_ CLIPPLANEENABLE                  | 0                      |
| D3DRS \_ puntuación                        | Dependiente del controlador       |
| D3DRS de \_ puntuación \_ mín.                   | 1                      |
| D3DRS \_ POINTSPRITEENABLE                | **FALSE**              |
| D3DRS \_ POINTSCALEENABLE                 | **FALSE**              |
| D3DRS \_ POINTSCALE \_                    | 1                      |
| D3DRS \_ POINTSCALE \_ B                    | 0                      |
| D3DRS \_ POINTSCALE \_ C                    | 0                      |
| D3DRS \_ MULTISAMPLEANTIALIAS             | **TRUE**               |
| D3DRS \_ MULTISAMPLEMASK                  | 0xFFFFFFFF             |
| D3DRS \_ PATCHEDGESTYLE                   | D3DPATCHEDGE \_ discreto |
| D3DRS \_ \_ Max                   | 1                      |
| D3DRS \_ INDEXEDVERTEXBLENDENABLE         | **FALSE**              |
| D3DRS \_ TWEENFACTOR                      | 0                      |
| D3DRS \_ POSITIONDEGREE                   | D3DDEGREE \_ cúbico       |
| D3DRS \_ NORMALDEGREE                     | \_Lineal D3DDEGREE      |
| D3DRS \_ MINTESSELLATIONLEVEL             | 1                      |
| D3DRS \_ MAXTESSELLATIONLEVEL             | 1                      |
| D3DRS \_ ADAPTIVETESS \_ X                  | 0                      |
| D3DRS \_ ADAPTIVETESS \_ Y                  | 0                      |
| D3DRS \_ ADAPTIVETESS \_ Z                  | 1                      |
| D3DRS \_ ADAPTIVETESS \_ W                  | 0                      |
| D3DRS \_ ENABLEADAPTIVETESSELLATION "/> | **FALSE**              |



 

## <a name="vertex-pipeline-sampler-state"></a>Canalización de vértices: estado de muestra

Los Estados de muestra controlan temas relacionados con el muestreo, como filtrado, mosaico y modos de dirección de coordenadas de textura. Use [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) para configurar el estado de la muestra (incluido el usado en la unidad del teselador para los mapas de desplazamiento de ejemplo). Se ha cambiado el nombre de los Estados de muestra con un \_ prefijo "D3DSAMP" para habilitar la detección de errores en tiempo de compilación al migrar desde DirectX 8.

En la tabla siguiente se incluyen todos los Estados de muestra que establecen el estado del vértice:



| Estados de muestra      | Valor predeterminado |
|---------------------|---------------|
| D3DSAMP \_ DMAPOFFSET | 256           |



 

## <a name="vertex-pipeline-texture-state"></a>Canalización de vértices: estado de textura

Los Estados de textura controlan las operaciones de combinación de texturas del mezclador de varias texturas. Use [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) para configurar los Estados de textura. Use [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para asociar una textura a una fase de muestra.

En la tabla siguiente se incluyen todos los Estados de textura que establecen el estado del vértice:



| Estados de textura                | Valor predeterminado    |
|-------------------------------|------------------|
| D3DTSS \_ TEXCOORDINDEX         | 0                |
| D3DTSS \_ TEXTURETRANSFORMFLAGS | Deshabilitación de D3DTTFF \_ |



 

D3DTSS \_ TEXCOORDINDEX es un estado de procesamiento de vértice de función fijo. Si se usa un sombreador de vértices programable, se omite este estado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estado de guardado y restauración de bloques de estado](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
