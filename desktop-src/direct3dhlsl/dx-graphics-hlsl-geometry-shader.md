---
title: Objeto Geometry-Shader
description: Un objeto de sombreador de geometría procesa los primitivos completos. Use la siguiente sintaxis para declarar un objeto de sombreador de geometría.
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- maxvertexcount (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadb0e8bb3ddda16305ac701b34523668bd9c1a5
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2019
ms.locfileid: "103785290"
---
# <a name="geometry-shader-object"></a>Objeto Geometry-Shader

Un objeto de sombreador de geometría procesa los primitivos completos. Use la siguiente sintaxis para declarar un objeto de sombreador de geometría.



|                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|
| \[maxvertexcount (*NumVerts*) \] void *ShaderName* ( *PrimitiveType DataType name \[ NumElements \]*, INOUT *StreamOutputObject* ); |



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount (*NumVerts*)\]
</dt> <dd>

\[en \] la declaración del número máximo de vértices que se van a crear.

-   \[maxvertexcount () \] : palabra clave required; los corchetes y los paréntesis son caracteres necesarios para la sintaxis correcta.
-   *NumVerts* : número entero que representa el número de vértices.

</dd> <dt>

<span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*
</dt> <dd>

\[en \] una cadena ASCII que contiene un nombre único para la función de sombreador de geometría.

</dd> <dt>

<span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType nombre del tipo de \[ NumElements \]*
</dt> <dd>

*PrimitiveType* : tipo primitivo, que determina el orden de los datos primitivos.



| Tipo primitivo | Descripción                                                   |
|----------------|---------------------------------------------------------------|
| *Elija*        | Lista de puntos                                                    |
| *Ondula*         | Lista de líneas o franja de líneas                                       |
| *ubicado*     | Lista de triángulos o franja de triángulo                               |
| *lineadj*      | Lista de líneas con proximidad o franja de línea con adyacencias         |
| *triangleadj*  | Lista de triángulos con banda de proximidad o triángulo con adyacencias |



 

  -  DataType \[ en \] un tipo de datos de entrada; puede ser cualquier [tipo de datos HLSL](dx-graphics-hlsl-data-types.md).

*Nombre* : nombre del argumento; se trata de una cadena ASCII.

*NumElements* : tamaño de la matriz de la entrada, que depende de *PrimitiveType* , tal como se muestra en la tabla siguiente.

| Tipo primitivo | NumElements                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| *Elija*        | \[1\]<br/> Solo se trabaja en un punto cada vez.<br/>                                         |
| *Ondula*         | \[2\]<br/> Una línea requiere dos vértices.<br/>                                                    |
| *ubicado*     | \[3\]<br/> Un triángulo requiere tres vértices.<br/>                                              |
| *lineadj*      | \[4\]<br/> Un lineadj tiene dos extremos; por lo tanto, requiere cuatro vértices.<br/>                    |
| *triangleadj*  | \[6\]<br/> Un triangleadj borde tres triángulos más. por lo tanto, requiere seis vértices.<br/> |



 

</dd> <dt>

<span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*
</dt> <dd>

La declaración del [objeto de salida de flujo](dx-graphics-hlsl-so-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

None

## <a name="remarks"></a>Observaciones

En el diagrama siguiente se muestran los distintos tipos primitivos para un objeto de sombreador de geometría.

![Ilustración de los distintos tipos primitivos para un objeto de sombreador de geometría](images/d3d11-gsinputs1.png)

En el diagrama siguiente se muestran las invocaciones del sombreador de geometría.

![Ilustración de las invocaciones del sombreador de geometría](images/d3d11-gsinputs2.png)

## <a name="examples"></a>Ejemplos

Este ejemplo procede del ejercicio 1 del [taller del modelo de sombreador de Direct3D 10 4,0](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Este objeto es compatible con los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 4](dx-graphics-hlsl-sm4.md) y versiones posteriores | sí       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





