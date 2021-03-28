---
title: Direccionamiento relativo (referencia de PS de HLSL)
description: La sintaxis \ \ solo se puede usar en tipos de registro que se pueden tratar relativamente en determinados modelos de sombreador.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38c7be68245cfedbb27898e0fbb689e9e43755ca
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "103785063"
---
# <a name="relative-addressing-hlsl-ps-reference"></a>Direccionamiento relativo (referencia de PS de HLSL)

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



| Tipo de registro                                                                                   | Versiones del sombreador de píxeles |
|-------------------------------------------------------------------------------------------------|-----------------------|
| [contador de bucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md): al en registros de entrada | PS \_ 3 \_ 0 y versiones posteriores   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




