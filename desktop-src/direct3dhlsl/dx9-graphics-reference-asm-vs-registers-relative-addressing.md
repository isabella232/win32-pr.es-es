---
title: Direccionamiento relativo (HLSL VS Reference)
description: La sintaxis \ \ solo se puede usar en tipos de registro que se pueden tratar relativamente en determinados modelos de sombreador.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c11d6f6c4b448e1dee5f4237696c110519bc0dd0
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104358522"
---
# <a name="relative-addressing-hlsl-vs-reference"></a>Direccionamiento relativo (HLSL VS Reference)

La \[ \] Sintaxis solo se puede usar en tipos de registro que se pueden tratar relativamente en determinados modelos de sombreador. Los formatos de sintaxis admitidos \[ \] se enumeran de la siguiente manera:

Donde:

-   "R" denota cualquier tipo de registro que pueda ser relativamente direccionado.
-   "A" denota cualquier registro que se puede utilizar como índice para abordar otros registros de forma relativamente.
-   N0-ni, M0-MJ y k son enteros >= 0.



| \[\]Sintaxis de                              | Índice efectivo                       | Ejemplos                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| R \[ A + M0 +... + MJ \]                  | A + M0 +... + MJ                     | c \[ a0. x + 3 + 7 \]              |
| R \[ k \] (= RK)                         | k                                     | c \[ 10 \] (= C10)              |
| R \[ A \]                                  | Un                                     | c \[ a0. y \]                      |
| RK \[ N0 +... + ni + A + M0 +... + MJ \] | A + k + N0 +... + ni + M0 +... + MJ | C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \] |
| R \[ N0 +... + ni + A + M0 +... + MJ \]  | A + N0 +... + ni + M0 +... + MJ     | c \[ 2 + 1 + al + 3 + 4 + 5 \]    |
| RK \[ A \]                                 | A + k                                 | C12 \[ al \] , C0 \[ a0. z \]        |
| RK \[ A + M0 +... + MJ \]                 | A + k + M0 +... + MJ                 | v1 \[ al + 4 + 8 \]               |
| R \[ N0 +... + ni + A \]                  | A + N0 +... + ni                     | o \[ 3 + 1 + al \]                |
| RK \[ N0 +... + ni + A \]                 | A + k + N0 +... + ni                 | O1 \[ 2 + 1 + 3 + al \]           |



 

Los registros están disponibles en las siguientes versiones:



| Tipo de registro | Versiones del sombreador de vértices |
|---------------|------------------------|
| a0            | All                    |
| Alabama            | vs \_ 2 \_ 0 y versiones posteriores    |
| cn            | vs \_ 1 \_ 1 y versiones posteriores    |
| on            | vs \_ 3 \_ 0               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




