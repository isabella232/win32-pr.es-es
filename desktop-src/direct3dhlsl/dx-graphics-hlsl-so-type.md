---
title: Stream-Output objeto
description: Un objeto stream-output es un objeto con plantilla que transmite datos fuera de la fase del sombreador de geometría. Use la sintaxis siguiente para declarar un objeto stream-output.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 79e0247b424ebb6f72622565845c17b622ab715cd8860a83ce24ae58ac7420c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789485"
---
# <a name="stream-output-object"></a>Stream-Output objeto

Un objeto stream-output es un objeto con plantilla que transmite datos fuera de la fase [del sombreador de geometría](/previous-versions//bb205146(v=vs.85)). Use la sintaxis siguiente para declarar un objeto stream-output.



| inout *StreamOutputObject* < *DataType* >  *Name;* |
|------------------------------------------------------|



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  <  *DataType*  >    *Nombre*
</dt> <dd>

Declaración del objeto stream-output (SO).



| Stream-Output de objetos | Descripción                       |
|----------------------------|-----------------------------------|
| *PointStream*              | Secuencia de primitivas de punto    |
| *LineStream*               | Secuencia de primitivas de línea     |
| *TriangleStream*           | Una secuencia de primitivas de triángulo |



 

*DataType:* tipo de datos de salida; puede ser cualquier [tipo de datos HLSL](dx-graphics-hlsl-data-types.md). Debe ir entre corchetes angulares.

*Nombre:* nombre de variable; cadena ASCII que identifica de forma única el objeto.

</dd> </dl>

## <a name="example"></a>Ejemplo

Este es un ejemplo de una declaración de objeto de salida de flujo que transmite primitivas de triángulo cuyos datos se definen mediante la estructura \_ PS CUBEMAP \_ IN. El sombreador de geometría se limita a generar 18 vértices.


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

Use la sintaxis siguiente para llamar a métodos stream-output-object.


```
Object.Method
```



Se implementan los métodos siguientes.



| Métodos                                              | Descripción                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [Append](dx-graphics-hlsl-so-append.md)             | Anexe los datos de salida a una secuencia existente.                        |
| [RestartStrip](dx-graphics-hlsl-so-restartstrip.md) | Finalice la franja primitiva actual e inicie una nueva franja primitiva. |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) y modelos de sombreador posteriores | Sí       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 