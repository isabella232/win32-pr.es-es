---
title: dcl_maxOutputVertexCount (SM4-ASM)
description: DCL \_ maxOutputVertexCount (SM4-ASM)
ms.assetid: 91eb2dfc-f4ff-4f23-9cb4-ec5fdb676157
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31a09788b2f407673f57dad8a71792a5b02b7613
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996980"
---
# <a name="dcl_maxoutputvertexcount-sm4---asm"></a>DCL \_ maxOutputVertexCount (SM4-ASM)

Declara el número máximo de vértices que puede generar un sombreador de geometría.



| recuento de maxOutputVertexCount de DCL \_  |
|-----------------------------------|



 



| Elemento                                                               | Descripción                                                             |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="count"></span><span id="COUNT"></span>*contabiliza*<br/> | \[en \] un entero sin signo de 32 bits comprendido entre 1 y n, ambos incluidos.<br/> |



 

Un sombreador de geometría puede generar un máximo de valores de 1024 32 bits. Este máximo incluye el tamaño de los datos de entrada y el tamaño de los datos creados por el sombreador.

Estas son algunas limitaciones:

-   Si se alcanza el número de vértices antes de que el sombreador de geometría termine de ejecutarse, el sombreador termina.
-   Un sombreador de geometría puede llegar al final de su programa antes de que se muestren los vértices; Esto es perfectamente válido.
-   Si va a depurar un sombreador de geometría, puede indicar el número de vértices que se generan al contar el número de instrucciones de emisión generadas.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               | x               |              |



 

Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.

## <a name="example"></a>Ejemplo

Estos son algunos ejemplos.

Asuma que los datos de entrada se componen de la posición (. xyzw) y del color (. RGB). Cada componente consume un byte; dados 7 bytes, el número máximo de vértices que puede generar el sombreador sería 1024/(4 + 3) = 146.


```
dcl_maxOutputVertexCount 146
```



Suponga que el sombreador de geometría crea vectores de componente 32 4. El número máximo de vértices que puede generar el sombreador sería 1024/(32 \* 4) = 8.


```
dcl_maxOutputVertexCount 8
```



## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





