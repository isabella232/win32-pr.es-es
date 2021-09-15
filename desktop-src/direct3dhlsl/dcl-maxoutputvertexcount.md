---
title: dcl_maxOutputVertexCount (sm4 - asm)
description: dcl \_ maxOutputVertexCount (sm4 - asm)
ms.assetid: 91eb2dfc-f4ff-4f23-9cb4-ec5fdb676157
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31a09788b2f407673f57dad8a71792a5b02b7613
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573916"
---
# <a name="dcl_maxoutputvertexcount-sm4---asm"></a>dcl \_ maxOutputVertexCount (sm4 - asm)

Declara el número máximo de vértices que puede generar un sombreador de geometría.



| dcl \_ maxOutputVertexCount *count* |
|-----------------------------------|



 



| Elemento                                                               | Descripción                                                             |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="count"></span><span id="COUNT"></span>*Contar*<br/> | \[en \] un entero de 32 bits sin signo entre 1 y n, ambos incluidos.<br/> |



 

Un sombreador de geometría puede generar un máximo de 1024 valores de 32 bits. Este máximo incluye el tamaño de los datos de entrada y el tamaño de los datos creados por el sombreador.

Estas son algunas limitaciones:

-   Si se alcanza el número de vértices antes de que finalice la ejecución del sombreador de geometría, el sombreador finaliza.
-   Un sombreador de geometría puede llegar al final de su programa antes de generar los vértices; esto es perfectamente legal.
-   Si está depurando un sombreador de geometría, puede decir el número de vértices generados contando el número de instrucciones de emisión generadas.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               | x               |              |



 

Esta instrucción se incluye para ayudar a depurar un sombreador en el ensamblado; No se puede crear un sombreador en el lenguaje de ensamblado mediante El modelo de sombreador 4.

## <a name="example"></a>Ejemplo

Estos son algunos ejemplos.

Suponga que los datos de entrada están hechos de posición (.xyzw) y color (.rgb). Cada componente consume un byte; Dados 7 bytes, el número máximo de vértices que puede generar el sombreador sería 1024 / (4 + 3) = 146.


```
dcl_maxOutputVertexCount 146
```



Supongamos que el sombreador de geometría crea 32 vectores de 4 componentes. El número máximo de vértices que puede generar el sombreador sería 1024 / (32 \* 4) = 8.


```
dcl_maxOutputVertexCount 8
```



## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





