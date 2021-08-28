---
title: Especificar destinos del compilador
description: Aquí se enumeran los destinos de varios perfiles que las funciones D3DCompile\ y el compilador HLSL admiten.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84d020edaabf4c618b1fa911a91bc4cc0e8b37e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481841"
---
# <a name="specifying-compiler-targets"></a>Especificar destinos del compilador

Debe especificar el destino del sombreador (conjunto de características de sombreador) con el que compilar al llamar a la función [**D3DCompile,**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)o [**D3DCompileFromFile.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) Aquí se enumeran los destinos de varios perfiles que las funciones **D3DCompile \*** y el compilador HLSL admiten.

-   [Niveles de características de Direct3D 11.0 y 11.1](#direct3d-110-and-111-feature-levels)
-   [Nivel de característica de Direct3D 10.1](#direct3d-101-feature-level)
-   [Nivel de característica de Direct3D 10.0](#direct3d-100-feature-level)
-   [Niveles de características de Direct3D 9.1, 9.2 y 9.3](#direct3d-91-92-and-93-feature-levels)
-   [Modelo de sombreador direct3D 9 heredado 3.0](#legacy-direct3d-9-shader-model-30)
-   [Modelo de sombreador direct3D 9 heredado 2.0](#legacy-direct3d-9-shader-model-20)
-   [Modelo de sombreador direct3D 9 heredado 1.x](#legacy-direct3d-9-shader-model-1x)
-   [Efectos heredados](#legacy-effects)
-   [Notas](#notes)
-   [Temas relacionados](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a>Niveles de características de Direct3D 11.0 y 11.1

Estos son los destinos del sombreador que admiten los niveles de características de Direct3D 11.0 [y](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.1.



| Destino   | Descripción                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 5 \_ 0 | DirectCompute 5.0[(sombreador de proceso)](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)                              |
| ds \_ 5 \_ 0 | [Sombreador de dominio](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| gs \_ 5 \_ 0 | [Sombreador de geometría](/previous-versions//bb205146(v=vs.85)) |
| hs \_ 5 \_ 0 | [Sombreador de casco](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| ps \_ 5 \_ 0 | [Sombreador de píxeles](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 5 \_ 0 | [Sombreador de vértices](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-101-feature-level"></a>Nivel de característica de Direct3D 10.1

Estos son los destinos del sombreador que [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) admite el nivel de características de Direct3D 10.1.



| Destino   | Descripción                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 4 \_ 1 | DirectCompute 4.1[(sombreador de proceso](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹                             |
| gs \_ 4 \_ 1 | [Sombreador de geometría](/previous-versions//bb205146(v=vs.85)) |
| ps \_ 4 \_ 1 | [Sombreador de píxeles](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 1 | [Sombreador de vértices](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-100-feature-level"></a>Nivel de característica de Direct3D 10.0

Estos son los destinos del sombreador que [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) admite el nivel de características de Direct3D 10.0.



| Destino   | Descripción                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 4 \_ 0 | DirectCompute 4.0[(sombreador de proceso](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹                             |
| gs \_ 4 \_ 0 | [Sombreador de geometría](/previous-versions//bb205146(v=vs.85)) |
| ps \_ 4 \_ 0 | [Sombreador de píxeles](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 0 | [Sombreador de vértices](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a>Niveles de características de Direct3D 9.1, 9.2 y 9.3

Estos son los destinos del sombreador que admiten los niveles de características direct3D 9.1, 9.2 [y](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9.3.

> [!Note]  
> Cuando se usan los perfiles de sombreador HLSL de nivel 4 0 de 9 x , se usan implícitamente los perfiles del modelo de sombreador 2.x para admitir hardware compatible con \* \_ \_ \_ \_ \_ Direct3D 9. [](dx-graphics-hlsl-sm2.md) Los perfiles del modelo de sombreador 2.x admiten un comportamiento de control de flujo más limitado que el modelo de sombreador [4.x](dx-graphics-hlsl-sm4.md) y los perfiles posteriores.

 




| Destino | Descripción | 
|--------|-------------|
| ps_4_0_level_9_1 | [Sombreador de](/previous-versions//bb205146(v=vs.85)) píxeles para 9.1 y 9.2 (límites similares a ps_2_0)<ul><li>64 instrucciones aritméticas y 32 de textura</li><li>12 registros temporales</li><li>4 niveles de lecturas dependientes</li></ul> | 
| ps_4_0_level_9_3 | <a href="/previous-versions//bb205146(v=vs.85)">Sombreador de</a> píxeles para la versión 9.3 (límites similares a ps_2_x además de características de sombreador)<ul><li>512 instrucciones</li><li>32 registros temporales</li><li>Control de flujo estático (profundidad máxima de 4)</li><li>Control de flujo dinámico (profundidad máxima de 24)</li><li>D3DPS20CAPS_ARBITRARYSWIZZLE</li><li>D3DPS20CAPS_GRADIENTINSTRUCTIONS</li><li>D3DPS20CAPS_PREDICATION</li><li>D3DPS20CAPS_NODEPENDENTREADLIMIT</li><li>D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</li></ul> | 
| vs_4_0_level_9_1 | <a href="/previous-versions//bb205146(v=vs.85)">Sombreador de</a> vértices para 9.1 y 9.2 (similar a vs_2_0)<ul><li>256 instrucciones</li><li>12 registros temporales</li><li>Control de flujo estático (profundidad máxima de 1)</li></ul> | 
| vs_4_0_level_9_3 | <a href="/previous-versions//bb205146(v=vs.85)">Sombreador de</a> vértices para 9.3 (similar a vs_2_a ndo con características de sombreador adicionales e instancias)<ul><li>256 instrucciones</li><li>32 registros temporales</li><li>Control de flujo estático (profundidad máxima de 4)</li><li>D3DVS20CAPS_PREDICATION</li></ul> | 




 

## <a name="legacy-direct3d-9-shader-model-30"></a>Modelo de sombreador direct3D 9 heredado 3.0

Estos son los destinos del sombreador para el modelo de sombreador 3.0 además de Direct3D 9 heredado.



| Destino    | Descripción                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| ps \_ 3 \_ 0  | [Sombreador de](/previous-versions//bb205146(v=vs.85)) píxeles 3.0               |
| ps \_ 3 \_ sw | [Sombreador de](/previous-versions//bb205146(v=vs.85)) píxeles 3.0 (software)    |
| vs \_ 3 \_ 0  | [Sombreador de](/previous-versions//bb205146(v=vs.85)) vértices 3.0            |
| vs \_ 3 \_ sw | [Sombreador de](/previous-versions//bb205146(v=vs.85)) vértices 3.0 (software) |



 

## <a name="legacy-direct3d-9-shader-model-20"></a>Modelo de sombreador direct3D 9 heredado 2.0

Estos son los destinos del sombreador para el modelo de sombreador direct3D 9 heredado 2.0 bytes.



| Destino    | Descripción                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| ps \_ 2 \_ 0  | [Sombreador de](/previous-versions//bb205146(v=vs.85)) píxeles 2.0             |
| ps \_ 2 \_ a  | [Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 2a              |
| ps \_ 2 \_ b  | [Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 2b              |
| ps \_ 2 \_ sw | [Software de sombreador](/previous-versions//bb205146(v=vs.85)) de píxeles 2.0    |
| vs \_ 2 \_ 0  | [Sombreador de](/previous-versions//bb205146(v=vs.85)) vértices 2.0          |
| vs \_ 2 \_ a  | [Sombreador de vértices](/previous-versions//bb205146(v=vs.85)) 2a           |
| vs \_ 2 \_ sw | Software [del sombreador](/previous-versions//bb205146(v=vs.85)) de vértices 2.0 |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a>Modelo de sombreador direct3D 9 heredado 1.x

Estos son los destinos del sombreador para el modelo de sombreador 1.x heredado de Direct3D 9⁴.



| Destino   | Descripción                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| tx \_ 1 \_ 0 | Perfil de sombreador de textura que usan las funciones D3DX9⁵ [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) y [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) heredadas |
| vs \_ 1 \_ 1 | [Sombreador de](/previous-versions//bb205146(v=vs.85)) vértices 1.1                                                            |



 

## <a name="legacy-effects"></a>Efectos heredados

Estos son los destinos de efecto de los efectos heredados.



| Destino   | Descripción                               |
|----------|-------------------------------------------|
| fx \_ 2 \_ 0 | Efectos (FX) para Direct3D 9 en D3DX9⁵     |
| fx \_ 4 \_ 0 | Efectos (FX) para Direct3D 10.0 en D3DX10⁵ |
| fx \_ 4 \_ 1 | Efectos (FX) para Direct3D 10.1 en D3DX10⁵ |
| fx \_ 5 \_ 0 | Efectos (FX) para Direct3D 11⁵             |



 

## <a name="notes"></a>Notas

Estas son algunas notas a las que hacen referencia las secciones anteriores:

1.  [Los dispositivos](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de nivel de característica 10.0 y 10.1 pueden admitir opcionalmente DirectCompute. Para comprobar la compatibilidad, use [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con [**D3D11 \_ FEATURE \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).
2.  [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) nivel de característica 9.3 requiere de forma eficaz hardware que cumpla los requisitos del modelo de sombreador [3.0 heredado de Direct3D 9,](#legacy-direct3d-9-shader-model-30)pero este nivel de característica no hace uso de destinos frente a \_ 3 0 o ps \_ \_ 3 \_ 0.
3.  Use solo modelos de sombreador heredados de Direct3D 9 con la API de Direct3D 9. En su lugar, use los perfiles 9.x con la API 10.x y 11.x de Direct3D.
4.  Las funciones **D3DCompile \*** del sombreador HLSL actual no admiten sombreadores de píxeles heredados de 1.x. La última versión de HLSL que admite estos destinos fue D3DX9 en la versión de octubre de 2006 del SDK de DirectX.
5.  Todas las versiones de D3DX y el SDK de DirectX están en desuso. Para obtener más información, [consulte ¿Dónde está el SDK de DirectX?](/windows/desktop/directx-sdk--august-2009-).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 
