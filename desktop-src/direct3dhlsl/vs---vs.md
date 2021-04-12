---
title: vs
description: Esta instrucción especifica el número de versión del sombreador. Esta instrucción funciona en todas las versiones de sombreador.
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: baf773d7607aa575bd575339bde072b3dc04b224
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419981"
---
# <a name="vs"></a>vs

Esta instrucción especifica el número de versión del sombreador. Esta instrucción funciona en todas las versiones de sombreador.

## <a name="syntax"></a>Sintaxis


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a>Argumentos de entrada

Los argumentos de entrada contienen un único número de versión principal con un único número de versión. Las combinaciones permitidas se muestran en la tabla siguiente.



| Versiones principales | Versiones secundarias                   |
|---------------|--------------------------------|
| 1             | 1                              |
| 2             | 0, SW (software), x (extendido) |
| 3             | 0, SW (software)               |



 

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| vs                     | x    | x    | x    | x     | x    | x     |



 

Esta instrucción debe ser la primera instrucción que no sea de comentario en un sombreador de vértices.

Esta instrucción es compatible con todas las versiones del sombreador de vértices.

Las versiones aceleradas de hardware del software (versiones sin \_ software en el número de versión), pueden procesar vértices con accelearation de hardware o usar el procesamiento de vértices de software. Las versiones de software (versiones con \_ SW en el número de versión) solo procesan los vértices con software.

## <a name="examples"></a>Ejemplos

Este ejemplo parcial declara un sombreador de vértices de la versión 1 \_ 1.


```
vs_1_1
```



Este ejemplo parcial declara un sombreador de vértices de software de la versión 2.


```
vs_2_sw
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




