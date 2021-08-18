---
title: vs
description: Esta instrucción especifica el número de versión del sombreador. Esta instrucción funciona en todas las versiones del sombreador.
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3977e77c685adb3a181804c0db5b281ae3e54c6f085586023855259f532dde8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484235"
---
# <a name="vs"></a>vs

Esta instrucción especifica el número de versión del sombreador. Esta instrucción funciona en todas las versiones del sombreador.

## <a name="syntax"></a>Syntax


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a>Argumentos de entrada

Los argumentos de entrada contienen un único número de versión principal con un único número de sub version. Las combinaciones permitidos se enumeran en la tabla siguiente.



| Versiones principales | Sub versions                   |
|---------------|--------------------------------|
| 1             | 1                              |
| 2             | 0, sw (software), x (extendido) |
| 3             | 0, sw (software)               |



 

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| vs                     | x    | x    | x    | x     | x    | x     |



 

Esta instrucción debe ser la primera instrucción que no sea de comentario en un sombreador de vértices.

Esta instrucción se admite en todas las versiones del sombreador de vértices.

Las versiones aceleradas por hardware del software (versiones sin sw en el número de versión), pueden procesar vértices con aceleración de hardware o usar el procesamiento de vértices \_ de software. Las versiones de software (versiones con sw en el número de versión) procesan los \_ vértices solo con software.

## <a name="examples"></a>Ejemplos

En este ejemplo parcial se declara un sombreador de vértices de la \_ versión 1 1.


```
vs_1_1
```



En este ejemplo parcial se declara un sombreador de vértices de software de la versión 2.


```
vs_2_sw
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




