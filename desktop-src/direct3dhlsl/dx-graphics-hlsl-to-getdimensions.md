---
title: Getdimensions ((objeto de textura de HLSL de DirectX)
description: Obtiene la información de tamaño de la textura. El bloque de sintaxis muestra todos los parámetros que son posibles en la declaración del método. En la tabla de la sección comentarios se muestran los parámetros que se implementan para cada tipo de objeto de textura.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ad4be68049c92955c5ddb06a0c5eccfe2c26b77
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904282"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a>Getdimensions ((objeto de textura de HLSL de DirectX)

Obtiene la información de tamaño de la textura. El bloque de sintaxis muestra todos los parámetros que son posibles en la declaración del método. En la tabla de la sección comentarios se muestran los parámetros que se implementan para cada tipo de objeto de textura.



|                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------|
| void Object. Getdimensions ((UINT MipLevel, typeX width, typeX height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples); |



 

typeX denota que hay dos tipos posibles: **uint** o **float**.

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                               | Descripción                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*<br/>                                     | Cualquier tipo [de objeto de textura,](dx-graphics-hlsl-to-type.md) excepto un objeto de **búfer** .<br/>                                       |
| <span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*<br/>                             | \[en \] un índice de base cero que identifica el nivel de mipmap. Si no se usa este argumento, se supone el primer nivel de MIP.<br/> |
| <span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Ancho*<br/>                                         | \[\]el ancho de la textura, en textura.<br/>                                                                                     |
| <span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Alto*<br/>                                     | \[\]el alto de la textura, en textura.<br/>                                                                                    |
| <span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elemento*<br/>                             | \[\]el número de elementos de una matriz.<br/>                                                                               |
| <span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Amplia*<br/>                                         | \[\]profundidad de textura, en textura.<br/>                                                                                     |
| <span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*<br/>     | \[\]el número de niveles de mipmap.<br/>                                                                                      |
| <span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*<br/> | \[\]el número de muestras.<br/>                                                                                            |



 

## <a name="return-value"></a>Valor devuelto

None

## <a name="overloaded-methods"></a>Métodos sobrecargados

En esta tabla se enumeran todas las versiones diferentes del método; las versiones difieren en función del número de parámetros de entrada. Observe que para cada método que toma parámetros de entero, hay un método sobrecargado que toma parámetros de punto flotante.



| Tipo de Texture-Object | Parámetros de entrada                                                               |
|---------------------|--------------------------------------------------------------------------------|
| Texture1D           | UINT MipLevel, UINT width, UINT NumberOfLevels                                 |
| Texture1D           | Ancho de UINT                                                                     |
| Texture1D           | UINT MipLevel, ancho flotante, Float NumberOfLevels                               |
| Texture1D           | Ancho flotante                                                                    |
| Texture1DArray      | UINT MipLevel, UINT width, UINT Elements, UINT NumberOfLevels                  |
| Texture1DArray      | UINT width, elementos UINT                                                      |
| Texture1DArray      | UINT MipLevel, ancho flotante, elementos Float, Float NumberOfLevels               |
| Texture1DArray      | Ancho flotante, elementos Float                                                    |
| Texture2D           | UINT MipLevel, UINT width, UINT height, UINT NumberOfLevels                    |
| Texture2D           | UINT width, alto de UINT                                                        |
| Texture2D           | UINT MipLevel, ancho flotante, alto Float, Float NumberOfLevels                 |
| Texture2D           | Ancho flotante, alto flotante                                                      |
| Texture2DArray      | UINT MipLevel, UINT width, UINT height, UINT Elements, UINT NumberOfLevels     |
| Texture2DArray      | UINT width, UINT height, UINT (elementos)                                         |
| Texture2DArray      | UINT MipLevel, ancho flotante, alto Float, elementos Float, Float NumberOfLevels |
| Texture2DArray      | Ancho flotante, alto flotante, elementos Float                                      |
| Texture3D           | UINT MipLevel, UINT width, UINT height, UINT Depth, UINT NumberOfLevels        |
| Texture3D           | UINT width, UINT height, UINT Depth                                            |
| Texture3D           | UINT MipLevel, ancho flotante, alto flotante, profundidad Float, Float NumberOfLevels    |
| Texture3D           | Ancho flotante, alto flotante, profundidad de punto flotante                                         |
| TextureCube         | UINT MipLevel, UINT width, UINT height, UINT NumberOfLevels                    |
| TextureCube         | UINT width, alto de UINT                                                        |
| TextureCube         | UINT MipLevel, ancho flotante, alto Float, UINT NumberOfLevels                  |
| TextureCube         | Ancho flotante, alto flotante                                                      |
| TextureCubeArray    | UINT MipLevel, UINT width, UINT height, UINT Elements, UINT NumberOfLevels     |
| TextureCubeArray    | UINT width, UINT height, UINT (elementos)                                         |
| TextureCubeArray    | UINT MipLevel, ancho flotante, alto Float, elementos Float, Float NumberOfLevels |
| TextureCubeArray    | Ancho flotante, alto flotante, elementos Float                                      |
| Texture2DMS         | UINT width, UINT height, UINT samples                                          |
| Texture2DMS         | Ancho flotante, alto flotante, ejemplos Float                                       |
| Texture2DMSArray    | UINT width, UINT height, UINT (elementos), ejemplos de UINT                           |
| Texture2DMSArray    | Ancho flotante, alto Float, elementos Float, ejemplos Float                       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  Devuelve dimensiones para el nivel de mipmap más grande (inicial).
2.  TextureCubeArray está disponible en el modelo de sombreador 4,1 o superior.
3.  El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texture-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





