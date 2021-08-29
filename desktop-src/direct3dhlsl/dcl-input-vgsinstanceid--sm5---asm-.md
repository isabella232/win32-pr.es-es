---
title: dcl_input vGSInstanceID (sm5 - asm)
description: Habilite la creación de instancias del sombreador de geometría.
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81d0ec89be2d75b591315bd4b38ff495426d98e5ce941b2eb6bc9028ba647620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950635"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a>dcl \_ input vGSInstanceID (sm5 - asm)

Habilite la creación de instancias del sombreador de geometría.



| dcl \_ input vGSInstanceID, instanceCount |
|-----------------------------------------|



 



| Elemento                                                                                                                       | Descripción                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*<br/> | \[en \] El identificador de instancia.<br/>    |
| <span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*<br/> | \[en \] El recuento de instancias.<br/> |



 

## <a name="remarks"></a>Comentarios

El *parámetro instanceCount* de la declaración especifica cuántas instancias debe ejecutar el sombreador de geometría para cada primitiva de entrada. El valor máximo de *instanceCount* es 32.

El número máximo de vértices declarados para la salida, a través de [**dcl \_ maxOutputVertexCount,**](dcl-maxoutputvertexcount.md)se aplica individualmente a cada instancia.

El recuento de instancias de esta declaración, multiplicado por el número máximo de vértices por instancia a través de [**dcl \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), debe ser <= 1024.

La cantidad de datos que una instancia de sombreador de geometría determinada puede emitir es de 1024 valores máximos escalares, validados contando todos los escalares declarados para la entrada y multiplicándose por el recuento de vértices de salida declarado.

El uso de la creación de instancias del sombreador de geometría aumenta de forma eficaz la cantidad total de datos que se pueden emitir por primitiva de entrada. 1024 escalares para una sola instancia produce hasta 1024 32 escalares de datos de salida en todas las instancias del sombreador de geometría para una primitiva de \* entrada única. Sin embargo, mientras más instancias, menos vértices puede emitir cada instancia. Una sola instancia (sin creación de instancias) puede emitir 1024 vértices. Si declara 32 instancias, significa que cada instancia solo puede generar \* 1024/32 = 32 vértices.

La declaración de creación de instancias del sombreador de geometría pone a disposición del programa un registro de entrada de entero independiente de 32 bits, *vGSInstanceID*. Cada instancia del sombreador de geometría se identifica mediante el valor contenido en *vGSInstanceID* \[ 0,1,2... \] .

*vGSInstanceID no* forma parte de la matriz de vértices de entrada del sombreador de geometría (por ejemplo, 3 vértices al introducir un triángulo). El *registro vGSInstanceID* se sitúa por sí solo, como vPrimitiveID.

Cuando finaliza cada instancia del sombreador de geometría, hay un corte implícito en la topología de salida, por lo que las instancias consecutivas no dependen entre sí.

Aunque el hardware puede ejecutar cada instancia del sombreador de geometría en paralelo, la salida de todas las instancias al final se serializa como si todas las invocaciones del sombreador de geometría con instancias se ejecutaran secuencialmente en un bucle que itera *vGSInstanceID* de 0 a *instanceCount*-1, con cortes de topología de salida implícitos al final de cada instancia.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





