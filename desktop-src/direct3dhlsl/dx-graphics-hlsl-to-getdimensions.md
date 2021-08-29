---
title: GetDimensions (objeto de textura HLSL de DirectX)
description: Obtiene información de tamaño de textura. El bloque de sintaxis muestra todos los parámetros posibles en la declaración de método. En la tabla de la sección Comentarios se muestran los parámetros que se implementan para cada tipo de objeto de textura.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e49c3c48ee71ecd86bcb28c763e06381aeb1a11b3c08ade8f7ec38f37048d21c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673445"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a>GetDimensions (objeto de textura HLSL de DirectX)

Obtiene información de tamaño de textura. El bloque de sintaxis muestra todos los parámetros posibles en la declaración de método. En la tabla de la sección Comentarios se muestran los parámetros que se implementan para cada tipo de objeto de textura.

void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );



 

typeX indica que hay dos tipos posibles: **uint** o **float.**

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                               | Descripción                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*<br/>                                     | Cualquier [tipo de objeto de](dx-graphics-hlsl-to-type.md) textura, excepto un objeto **Buffer.**<br/>                                       |
| <span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*<br/>                             | \[en \] Un índice de base cero que identifica el nivel de mapa mip. Si no se usa este argumento, se supone el primer nivel de mip.<br/> |
| <span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Ancho*<br/>                                         | \[out \] Ancho de textura, en texturas.<br/>                                                                                     |
| <span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Altura*<br/>                                     | \[out \] Alto de textura, en texturas.<br/>                                                                                    |
| <span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elementos*<br/>                             | \[out \] Número de elementos de una matriz.<br/>                                                                               |
| <span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Profundidad*<br/>                                         | \[out \] Profundidad de textura, en texturas.<br/>                                                                                     |
| <span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*<br/>     | \[out \] El número de niveles de mapa mip.<br/>                                                                                      |
| <span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*<br/> | \[out \] El número de muestras.<br/>                                                                                            |



 

## <a name="return-value"></a>Valor devuelto

None

## <a name="overloaded-methods"></a>Métodos sobrecargados

En esta tabla se enumeran todas las versiones diferentes del método ; las versiones difieren en el número de parámetros de entrada. Observe que para cada método que toma parámetros enteros, hay un método sobrecargado que toma parámetros de punto flotante.



| Texture-Object type | Parámetros de entrada                                                               |
|---------------------|--------------------------------------------------------------------------------|
| Texture1D           | UINT MipLevel, UINT Width, UINT NumberOfLevels                                 |
| Texture1D           | Ancho de UINT                                                                     |
| Texture1D           | UINT MipLevel, float Width, float NumberOfLevels                               |
| Texture1D           | float Width                                                                    |
| Texture1DArray      | UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels                  |
| Texture1DArray      | Ancho UINT, elementos UINT                                                      |
| Texture1DArray      | UINT MipLevel, float Width, float Elements, float NumberOfLevels               |
| Texture1DArray      | float Width, float Elements                                                    |
| Texture2D           | UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels                    |
| Texture2D           | UINT Width, UINT Height                                                        |
| Texture2D           | UINT MipLevel, float Width, float Height, float NumberOfLevels                 |
| Texture2D           | float Width, float Height                                                      |
| Texture2DArray      | UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels     |
| Texture2DArray      | UINT Width, UINT Height, UINT Elements                                         |
| Texture2DArray      | UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels |
| Texture2DArray      | float Width, float Height, float Elements                                      |
| Texture3D           | UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels        |
| Texture3D           | UINT Width, UINT Height, UINT Depth                                            |
| Texture3D           | UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels    |
| Texture3D           | float Width, float Height, float Depth                                         |
| TextureCube         | UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels                    |
| TextureCube         | UINT Width, UINT Height                                                        |
| TextureCube         | UINT MipLevel, float Width, float Height, UINT NumberOfLevels                  |
| TextureCube         | float Width, float Height                                                      |
| TextureCubeArray    | UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels     |
| TextureCubeArray    | UINT Width, UINT Height, UINT Elements                                         |
| TextureCubeArray    | UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels |
| TextureCubeArray    | float Width, float Height, float Elements                                      |
| Texture2DMS         | UINT Width, UINT Height, UINT Samples                                          |
| Texture2DMS         | float Width, float Height, float Samples                                       |
| Texture2DMSArray    | UINT Width, UINT Height, UINT Elements, UINT Samples                           |
| Texture2DMSArray    | float Width, float Height, float Elements, float Samples                       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  Devuelve dimensiones para el nivel de mapa mip más grande (cero).
2.  TextureCubeArray está disponible en Shader Model 4.1 o superior.
3.  El modelo de sombreador 4.1 está disponible en Direct3D 10.1 o superior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texture-Object](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





