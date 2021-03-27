---
title: dcl_input vGSInstanceID (SM5-ASM)
description: Habilitar la creación de instancias del sombreador de geometría.
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3134a9d372f1fde5457f26235fe9a6a5439c58c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358514"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a>\_vGSInstanceID de entrada de DCL (SM5-ASM)

Habilitar la creación de instancias del sombreador de geometría.



| \_entrada de DCL vGSInstanceID, instanceCount |
|-----------------------------------------|



 



| Elemento                                                                                                                       | Descripción                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*<br/> | \[en \] el ID. de instancia.<br/>    |
| <span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*<br/> | \[en \] el recuento de instancias.<br/> |



 

## <a name="remarks"></a>Observaciones

El parámetro *instanceCount* de la declaración especifica el número de instancias que el sombreador de geometría debe ejecutar para cada primitiva de entrada. El valor máximo de *instanceCount* es 32.

El número máximo de vértices declarado para la salida, a través de [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), se aplica individualmente a cada instancia.

El recuento de instancias en esta declaración, multiplicado por el número máximo de vértices por instancia a través de [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), debe ser <= 1024.

La cantidad de datos que puede emitir una instancia de sombreador de geometría determinada es 1024 escalares máximos, validados por el recuento de todos los escalares declarados para la entrada y la multiplicación por el número de vértices de salida declarado.

El uso de la creación de instancias del sombreador de geometría aumenta de forma eficaz la cantidad total de datos que se pueden emitir por primitiva de entrada. 1024 escalares para una instancia única produce hasta 1024 \* 32 escalares de datos de salida en todas las instancias de sombreador de geometría para un único primitivo de entrada. Sin embargo, cuantas más instancias haya, menos vértices podrá emitir cada instancia. Una sola instancia (sin creación de instancias) puede emitir vértices 1024. Si declara \* 32 instancias, significa que cada instancia solo puede generar los vértices 1024/32 = 32.

La declaración de creación de instancias del sombreador de geometría pone a disposición del programa un registro de entrada entero de 32 bits independiente, *vGSInstanceID*. Cada instancia del sombreador de geometría se identifica mediante el valor contenido en *vGSInstanceID* \[ 0, 1, 2... \] .

*vGSInstanceID* no forma parte de la matriz de vértices de entrada del sombreador de geometría (por ejemplo, 3 vértices al insertar un triángulo). El registro *vGSInstanceID* es propio, como vPrimitiveID.

Cuando finaliza cada instancia de sombreador de geometría, hay un corte implícito en la topología de salida, por lo que las instancias consecutivas no dependen unas de otras.

Aunque el hardware puede ejecutar cada instancia del sombreador de geometría en paralelo, la salida de todas las instancias del extremo se serializa como si todas las invocaciones del sombreador de geometría con instancias se ejecutaran secuencialmente en un bucle que recorre *vGSInstanceID* de 0 a *instanceCount*-1, con cortes de topología de salida implícitos al final de cada instancia.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





