---
title: Especificar destinos del compilador
description: Aquí se enumeran los destinos para varios perfiles que admiten las funciones D3DCompile y el compilador de HLSL.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68fc6c5a202ad537b02a20846d36526533240f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421349"
---
# <a name="specifying-compiler-targets"></a>Especificar destinos del compilador

Debe especificar el destino del sombreador (conjunto de características del sombreador) para compilar con cuando llame a la función [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)o [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) . Aquí se enumeran los destinos para varios perfiles que admiten las funciones **D3DCompile \*** y el compilador de HLSL.

-   [Niveles de características de Direct3D 11,0 y 11,1](#direct3d-110-and-111-feature-levels)
-   [Nivel de características de Direct3D 10,1](#direct3d-101-feature-level)
-   [Nivel de características de Direct3D 10,0](#direct3d-100-feature-level)
-   [Niveles de características de Direct3D 9,1, 9,2 y 9,3](#direct3d-91-92-and-93-feature-levels)
-   [Modelo de sombreador de Direct3D 9 heredado 3,0](#legacy-direct3d-9-shader-model-30)
-   [Modelo de sombreador de Direct3D 9 heredado 2,0](#legacy-direct3d-9-shader-model-20)
-   [Modelo 1. x del sombreador de Direct3D 9 heredado](#legacy-direct3d-9-shader-model-1x)
-   [Efectos heredados](#legacy-effects)
-   [Notas](#notes)
-   [Temas relacionados](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a>Niveles de características de Direct3D 11,0 y 11,1

Estos son los destinos del sombreador que admiten [los niveles de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de Direct3D 11,0 y 11,1.



| Destino   | Descripción                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 5 \_ 0 | DirectCompute 5,0 ([sombreador de cálculo](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))                              |
| DS \_ 5 \_ 0 | [Sombreador de dominios](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| GS \_ 5 \_ 0 | [Sombreador de geometría](/previous-versions//bb205146(v=vs.85)) |
| HS \_ 5 \_ 0 | [Sombreador de casco](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| PS \_ 5 \_ 0 | [Sombreador de píxeles](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 5 \_ 0 | [Sombreador de vértices](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-101-feature-level"></a>Nivel de características de Direct3D 10,1

Estos son los destinos del sombreador que admite el [nivel de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de Direct3D 10,1.



| Destino   | Descripción                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 4 \_ 1 | DirectCompute 4,1 ([sombreador de cálculo](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| GS \_ 4 \_ 1 | [Sombreador de geometría](/previous-versions//bb205146(v=vs.85)) |
| PS \_ 4 \_ 1 | [Sombreador de píxeles](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 1 | [Sombreador de vértices](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-100-feature-level"></a>Nivel de características de Direct3D 10,0

Estos son los destinos del sombreador que admite el [nivel de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de Direct3D 10,0.



| Destino   | Descripción                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 4 \_ 0 | DirectCompute 4,0 ([sombreador de cálculo](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| GS \_ 4 \_ 0 | [Sombreador de geometría](/previous-versions//bb205146(v=vs.85)) |
| PS \_ 4 \_ 0 | [Sombreador de píxeles](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 0 | [Sombreador de vértices](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a>Niveles de características de Direct3D 9,1, 9,2 y 9,3

Estos son los destinos del sombreador que admiten [los niveles de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de Direct3D 9,1, 9,2 y 9,3.

> [!Note]  
> Cuando se usan los \* \_ \_ perfiles del \_ \_ \_ sombreador HLSL de 4 0 nivel 9 x, se usan implícitamente los perfiles del [modelo de sombreador 2. x](dx-graphics-hlsl-sm2.md) para admitir el hardware compatible con Direct3D 9. Los perfiles del modelo de sombreador 2. x admiten un comportamiento de control de flujo más limitado que los perfiles del [modelo de sombreador 4. x](dx-graphics-hlsl-sm4.md) y posteriores.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Destino</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ps_4_0_level_9_1</td>
<td>[Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) para 9,1 y 9,2 (límites similares a ps_2_0)
<ul>
<li>64 instrucciones de textura aritmética y 32</li>
<li>12 registros temporales</li>
<li>4 niveles de lecturas dependientes</li>
</ul></td>
</tr>
<tr class="even">
<td>ps_4_0_level_9_3</td>
<td><a href="/previous-versions//bb205146(v=vs.85)">Sombreador de píxeles</a> para 9,3 (límites similares a ps_2_x ² con características adicionales del sombreador)
<ul>
<li>512 instrucciones</li>
<li>32 registros temporales</li>
<li>Control de flujo estático (profundidad máxima de 4)</li>
<li>Control de flujo dinámico (profundidad máxima de 24)</li>
<li>D3DPS20CAPS_ARBITRARYSWIZZLE</li>
<li>D3DPS20CAPS_GRADIENTINSTRUCTIONS</li>
<li>D3DPS20CAPS_PREDICATION</li>
<li>D3DPS20CAPS_NODEPENDENTREADLIMIT</li>
<li>D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</li>
</ul></td>
</tr>
<tr class="odd">
<td>vs_4_0_level_9_1</td>
<td><a href="/previous-versions//bb205146(v=vs.85)">Sombreador de vértices</a> para 9,1 y 9,2 (similar a vs_2_0)
<ul>
<li>256 instrucciones</li>
<li>12 registros temporales</li>
<li>Control de flujo estático (profundidad máxima de 1)</li>
</ul></td>
</tr>
<tr class="even">
<td>vs_4_0_level_9_3</td>
<td><a href="/previous-versions//bb205146(v=vs.85)">Sombreador de vértices</a> para 9,3 (similar a vs_2_a ² con características adicionales del sombreador y creación de instancias)
<ul>
<li>256 instrucciones</li>
<li>32 registros temporales</li>
<li>Control de flujo estático (profundidad máxima de 4)</li>
<li>D3DVS20CAPS_PREDICATION</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="legacy-direct3d-9-shader-model-30"></a>Modelo de sombreador de Direct3D 9 heredado 3,0

Estos son los destinos del sombreador para el modelo de sombreador de Direct3D 9 heredado 3,0 ³.



| Destino    | Descripción                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| PS \_ 3 \_ 0  | [Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 3,0               |
| PS \_ 3 \_ SW | [Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 3,0 (software)    |
| vs \_ 3 \_ 0  | [Sombreador de vértices](/previous-versions//bb205146(v=vs.85)) 3,0            |
| vs \_ 3 \_ SW | [Sombreador de vértices](/previous-versions//bb205146(v=vs.85)) 3,0 (software) |



 

## <a name="legacy-direct3d-9-shader-model-20"></a>Modelo de sombreador de Direct3D 9 heredado 2,0

Estos son los destinos del sombreador para el modelo de sombreador de Direct3D 9 heredado 2,0 ³.



| Destino    | Descripción                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| PS \_ 2 \_ 0  | [Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 2,0             |
| PS \_ 2 \_ a  | [Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 2A              |
| PS \_ 2 \_ b  | [Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 2B              |
| PS \_ 2 \_ SW | Software del [sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 2,0    |
| vs \_ 2 \_ 0  | [Sombreador de vértices](/previous-versions//bb205146(v=vs.85)) 2,0          |
| vs \_ 2 \_ a  | [Sombreador de vértices](/previous-versions//bb205146(v=vs.85)) 2A           |
| vs \_ 2 \_ SW | Software del [sombreador de vértices](/previous-versions//bb205146(v=vs.85)) 2,0 |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a>Modelo 1. x del sombreador de Direct3D 9 heredado

Estos son los destinos del sombreador para el modelo de sombreador de Direct3D 9 heredado 1. x ⁴.



| Destino   | Descripción                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TX \_ 1 \_ 0 | Perfil de sombreador de textura que hereda D3DX9 ⁵ Functions [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) y [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) use |
| vs \_ 1 \_ 1 | [Sombreador de vértices](/previous-versions//bb205146(v=vs.85)) 1,1                                                            |



 

## <a name="legacy-effects"></a>Efectos heredados

Estos son los objetivos de efecto de los efectos heredados.



| Destino   | Descripción                               |
|----------|-------------------------------------------|
| FX \_ 2 \_ 0 | Effects (FX) para Direct3D 9 en D3DX9 ⁵     |
| FX \_ 4 \_ 0 | Effects (FX) para Direct3D 10,0 en D3DX10 ⁵ |
| FX \_ 4 \_ 1 | Effects (FX) para Direct3D 10,1 en D3DX10 ⁵ |
| FX \_ 5 \_ 0 | Effects (FX) para Direct3D 11 ⁵             |



 

## <a name="notes"></a>Notas

A continuación se muestran algunas notas a las que se hace referencia en las secciones anteriores:

1.  los dispositivos de [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 y 10,1 pueden admitir opcionalmente DirectCompute. Para comprobar la compatibilidad, use [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con [**\_ \_ \_ \_ \_ las opciones de hardware D3D10 X de la característica D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).
2.  el [nivel de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9,3 requiere de forma eficaz hardware que cumpla los requisitos del modelo de [sombreador de Direct3D 9 heredado 3,0](#legacy-direct3d-9-shader-model-30), pero este nivel de característica no hace uso de los destinos vs \_ 3 \_ 0 o PS \_ 3 \_ 0.
3.  Use solo modelos de sombreador de Direct3D 9 heredados con la API de Direct3D 9. En su lugar, use los perfiles 9. x con la API Direct3D 10. x y 11. x.
4.  Las funciones **D3DCompile \*** del sombreador de HLSL actuales no admiten los sombreadores de píxeles de 1. x heredados. La última versión de HLSL para admitir estos destinos se D3DX9 en la versión de octubre de 2006 del SDK de DirectX.
5.  Todas las versiones de D3DX y el SDK de DirectX están en desuso. Para obtener más información, vea [¿Dónde está el SDK de DirectX?](/windows/desktop/directx-sdk--august-2009-).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 