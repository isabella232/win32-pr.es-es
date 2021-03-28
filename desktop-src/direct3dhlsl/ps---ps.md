---
title: ps
description: Esta instrucción especifica el número de versión del sombreador y funciona en todas las versiones del sombreador.
ms.assetid: 953b1d66-09c1-4ad5-96d4-acb49a1f244c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdf251d8b5618916365348ab3bf62a89ea552de1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996964"
---
# <a name="ps"></a>ps

Esta instrucción especifica el número de versión del sombreador y funciona en todas las versiones del sombreador.

## <a name="syntax"></a>Sintaxis


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a>Argumentos de entrada

Los argumentos de entrada contienen un único número de versión principal con un único número de versión. Las combinaciones permitidas se muestran en la tabla siguiente.



| Versiones principales | Versiones secundarias                   |
|---------------|--------------------------------|
| 1             | 1, 2, 3, 4                     |
| 2             | 0, x (extendido), SW (software) |
| 3             | 0, SW (software)               |



 

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| ps                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Esta instrucción debe ser la primera instrucción que no sea de comentario en un sombreador de píxeles.

Las versiones aceleradas de hardware del software (versiones sin \_ software en el número de versión), pueden procesar vértices con accelearation de hardware o usar el procesamiento de vértices de software. Las versiones de software (versiones con \_ SW en el número de versión) solo procesan los vértices con software.

## <a name="examples"></a>Ejemplos

Este ejemplo parcial declara un sombreador de píxeles de la versión 1 \_ 1.


```
ps_1_1
```



Este ejemplo parcial declara un sombreador de cuatro píxeles de la versión 1 \_ .


```
ps_1_4
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




