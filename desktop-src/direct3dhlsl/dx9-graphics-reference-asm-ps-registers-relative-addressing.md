---
title: Direccionamiento relativo (referencia de HLSL PS)
description: En el caso de los sombreadores de píxeles, la sintaxis \ \ solo se puede usar en tipos de registro que se puedan abordar relativamente en determinados modelos de sombreador.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4333560cc146057a4760e21353906b0523fef54c887dd5ffc3b2b03eddfec86c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090091"
---
# <a name="relative-addressing-hlsl-ps-reference"></a>Direccionamiento relativo (referencia de HLSL PS)

La \[ \] sintaxis solo se puede usar en tipos de registro que se pueden abordar relativamente en determinados modelos de sombreador. Las formas de \[ \] sintaxis admitidas se enumeran de la siguiente manera:

Donde:

-   "R" denota cualquier tipo de registro que se pueda abordar relativamente.
-   "A" denota cualquier registro que se pueda usar como índice para dirigirse relativamente a otros registros.
-   n0 - ni, m0 - mj y k son enteros >= 0.



| Sintaxis de \[ \]                              | Índice efectivo                       | Ejemplos                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| R \[ A + m0 + ... + mj \]                  | A + m0 + ... + mj                     | c \[ a0.x + 3 + 7 \]              |
| R \[ k ( = \] Rk )                         | k                                     | c \[ 10 \] ( = c10 )              |
| R \[ A \]                                  | A                                     | c \[ a0.y \]                      |
| Rk \[ n0 + ... + ni + A + m0 + ... + mj \] | A + k + n0 + ... + ni + m0 + ... + mj | c8 \[ 3 + 2 + a0.w + 5 + 6 + 1 \] |
| R \[ n0 + ... + ni + A + m0 + ... + mj \]  | A + n0 + ... + ni + m0 + ... + mj     | c \[ 2 + 1 + aL + 3 + 4 + 5 \]    |
| Rk \[ A \]                                 | A + k                                 | c12 \[ aL \] , c0 \[ a0.z \]        |
| Rk \[ A + m0 + ... + mj \]                 | A + k + m0 + ... + mj                 | v1 \[ aL + 4 + 8 \]               |
| R \[ n0 + ... + ni + A \]                  | A + n0 + ... + ni                     | o \[ 3 + 1 + aL \]                |
| Rk \[ n0 + ... + ni + A \]                 | A + k + n0 + ... + ni                 | o1 \[ 2 + 1 + 3 + aL \]           |



 

Los registros están disponibles en las siguientes versiones:



| Tipo de registro                                                                                   | Versiones del sombreador de píxeles |
|-------------------------------------------------------------------------------------------------|-----------------------|
| [contador de bucles:](dx9-graphics-reference-asm-ps-registers-loop-counter.md)aL en los registros de entrada | ps \_ 3 \_ 0 y superior   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




