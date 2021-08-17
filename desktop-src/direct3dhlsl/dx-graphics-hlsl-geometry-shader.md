---
title: Geometry-Shader objeto
description: Un objeto de sombreador de geometría procesa primitivas enteras. Use la sintaxis siguiente para declarar un objeto de sombreador de geometría.
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
ms.openlocfilehash: 5b95f0bb99bd3a225afb7a63824b301b102030a4f132caa7a2a4ff1743eefb58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120149"
---
# <a name="geometry-shader-object"></a>Geometry-Shader objeto

Un objeto de sombreador de geometría procesa primitivas enteras. Use la sintaxis siguiente para declarar un objeto de sombreador de geometría.

\[maxvertexcount(*NumVerts*) \] void *ShaderName* ( *PrimitiveType DataType Name \[ NumElements \]*, inout *StreamOutputObject* );



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]
</dt> <dd>

\[en \] Declaración para el número máximo de vértices que se crearán.

-   \[maxvertexcount(): palabra clave obligatoria; los corchetes y paréntesis son caracteres \] necesarios para la sintaxis correcta.
-   *NumVerts:* número entero que representa el número de vértices.

</dd> <dt>

<span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*
</dt> <dd>

\[en \] Una cadena ASCII que contiene un nombre único para la función geometry-shader.

</dd> <dt>

<span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*
</dt> <dd>

*PrimitiveType:* tipo primitivo, que determina el orden de los datos primitivos.



| Tipo primitivo | Descripción                                                   |
|----------------|---------------------------------------------------------------|
| *Punto*        | Lista de puntos                                                    |
| *Línea*         | Lista de líneas o franja de líneas                                       |
| *Triángulo*     | Lista de triángulos o franja de triángulos                               |
| *ydj*      | Lista de líneas con adyacencia o franja de línea con adyacencia         |
| *triangleadj*  | Lista de triángulos con adyacencia o franja de triángulo con adyacencia |



 

*DataType*  -  \[ en \] Un tipo de datos de entrada; puede ser cualquier tipo de datos [HLSL](dx-graphics-hlsl-data-types.md).

*Name:* nombre del argumento; se trata de una cadena ASCII.

*NumElements:* tamaño de matriz de la entrada, que depende de *PrimitiveType,* como se muestra en la tabla siguiente.

| Tipo primitivo | NumElements                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| *Punto*        | \[1\]<br/> Solo se trabaja en un punto a la vez.<br/>                                         |
| *Línea*         | \[2\]<br/> Una línea requiere dos vértices.<br/>                                                    |
| *Triángulo*     | \[3\]<br/> Un triángulo requiere tres vértices.<br/>                                              |
| *ydj*      | \[4\]<br/> Un resalte tiene dos extremos: por lo tanto, requiere cuatro vértices.<br/>                    |
| *triangleadj*  | \[6\]<br/> Un triánguloadj bordea tres triángulos más; por lo tanto, requiere seis vértices.<br/> |



 

</dd> <dt>

<span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*
</dt> <dd>

Declaración del objeto [stream-output](dx-graphics-hlsl-so-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

None

## <a name="remarks"></a>Observaciones

En el diagrama siguiente se muestran los distintos tipos primitivos para un objeto de sombreador de geometría.

![ilustración de los distintos tipos primitivos para un objeto de sombreador de geometría](images/d3d11-gsinputs1.png)

En el diagrama siguiente se muestran las invocaciones del sombreador de geometría.

![ilustración de las invocaciones del sombreador de geometría](images/d3d11-gsinputs2.png)

## <a name="examples"></a>Ejemplos

Este ejemplo es del ejercicio 1 del taller [Direct3D 10 Shader Model 4.0](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).


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



## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| [Modelos de sombreador 4](dx-graphics-hlsl-sm4.md) y superiores | Sí       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shader Model 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





