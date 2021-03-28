---
title: Modificadores de registro de origen del sombreador de vértices
description: Los modificadores de origen se pueden aplicar para modificar los datos leídos de un registro de origen antes de que la instrucción use los datos.
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c663741da50620e03cfde9f13d67a0c0063453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418912"
---
# <a name="vertex-shader-source-register-modifiers"></a>Modificadores de registro de origen del sombreador de vértices

Los modificadores de origen se pueden aplicar para modificar los datos leídos de un registro de origen antes de que la instrucción use los datos.

## <a name="negate"></a>Negate

Niega el contenido del registro de origen.



| Modificador de componente | Descripción     |
|--------------------|-----------------|
| \- c               | Negación de origen |



 

No se puede usar el modificador Negate en el segundo registro de código fuente de estas instrucciones: [m3x2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [M3x4-vs](m3x4---vs.md), [m4x3-vs](m4x3---vs.md), [M4x4-vs](m4x4---vs.md).



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| \-                     | x    | x    | x    | x     | x    | x     |



 

## <a name="absolute-value"></a>Valor absoluto

Tome el valor absoluto del registro.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| abs                    |      |      |      |       | x    | x     |



 

Si cualquier sombreador de la versión 3 Lee de uno o más registros Float constantes (c \# ), debe cumplirse una de las siguientes condiciones.

-   Todos los registros de punto flotante constantes deben usar el modificador ABS.
-   Ninguno de los registros de punto flotante constantes puede usar el modificador ABS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modificadores de registro del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




