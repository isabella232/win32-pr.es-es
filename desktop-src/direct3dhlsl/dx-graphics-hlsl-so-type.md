---
title: Objeto Stream-Output
description: Un objeto de salida de flujo es un objeto con plantilla que transmite los datos fuera de la fase del sombreador de geometría. Use la siguiente sintaxis para declarar un objeto de salida de flujo.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98063ddb45633dda6c897abf0f82f29a394c3f95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420866"
---
# <a name="stream-output-object"></a>Objeto Stream-Output

Un objeto de salida de flujo es un objeto con plantilla que transmite los datos fuera de la [fase del sombreador de geometría](/previous-versions//bb205146(v=vs.85)). Use la siguiente sintaxis para declarar un objeto de salida de flujo.



| nombre del tipo de *StreamOutputObject* INOUT <  >  *;* |
|------------------------------------------------------|



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  <  *DataType*  >    *Nombre* de
</dt> <dd>

La declaración del objeto de salida de flujo (SO).



| Stream-Output tipos de objeto | Descripción                       |
|----------------------------|-----------------------------------|
| *PointStream*              | Secuencia de primitivas de punto.    |
| *LineStream*               | Secuencia de primitivas de línea     |
| *TriangleStream*           | Secuencia de primitivas triangulares |



 

Tipo de datos *DataType* -Output; puede ser cualquier [tipo de datos HLSL](dx-graphics-hlsl-data-types.md). Debe ir entre corchetes angulares.

*Nombre* : nombre de la variable; cadena ASCII que identifica de forma única el objeto.

</dd> </dl>

## <a name="example"></a>Ejemplo

Este es un ejemplo de una declaración de objeto de salida de flujo que transmite los primitivos triángulos cuyos datos se definen mediante la \_ mapa \_ de PS en la estructura. El sombreador de geometría está limitado a la generación de 18 vértices.


```
struct PS_CUBEMAP_IN
{
    float4 Pos : SV_POSITION;     // Projection coord
    float2 Tex : TEXCOORD0;       // Texture coord
    uint RTIndex : SV_RenderTargetArrayIndex;
};

[maxvertexcount(18)]
void main( inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream, triangle PS_CUBEMAP_INT[3] )
{
    ...
}
```



Se trata de un fragmento de código del [ejemplo CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).

## <a name="stream-output-object-methods"></a>Stream-Output métodos de objeto

Use la siguiente sintaxis para llamar a los métodos Stream-Output-Object.


```
Object.Method
```



Se implementan los métodos siguientes.



| Métodos                                              | Descripción                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [Append](dx-graphics-hlsl-so-append.md)             | Anexe los datos de salida a un flujo existente.                        |
| [RestartStrip](dx-graphics-hlsl-so-restartstrip.md) | Finalizar la franja primitiva actual e iniciar una nueva banda primitiva. |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Este objeto es compatible con los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 4](dx-graphics-hlsl-sm4.md) y versiones posteriores | sí       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 