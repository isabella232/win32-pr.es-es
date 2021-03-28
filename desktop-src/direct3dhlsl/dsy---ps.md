---
title: DSY-PS
description: Calcula la tasa de cambio en la dirección y del destino de representación.
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5f595d836ed8eb8525175ddb81e743cb7a04811
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419907"
---
# <a name="dsy---ps"></a>DSY-PS

Calcula la tasa de cambio en la dirección y del destino de representación.

## <a name="syntax"></a>Sintaxis



| DSY DST, src |
|--------------|



 

Donde:

-   DST es un registro de destino.
-   src es un registro de origen de entrada.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dsy                   |      |      |      |      |      | x    | x     | x    | x     |



 

La tasa de cambio calculada a partir del registro de origen es una aproximación en el contenido del mismo registro en píxeles adyacentes que ejecutan el sombreador de píxeles en el paso de bloqueo con el píxel actual.

Las instrucciones [DSX](dsx---ps.md) y DSY calculan su resultado examinando el contenido actual del registro de origen (por componente) para los distintos píxeles del área local que se ejecuta en el paso de bloqueo. La fórmula exacta que se usa para calcular el degradado varía en función del hardware, pero debe ser coherente con la manera en que el hardware realiza las mismas operaciones como parte del proceso de cálculo del nivel de detalle para el muestreo de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[texldd-PS](texldd---ps.md)
</dt> </dl>

 

 




