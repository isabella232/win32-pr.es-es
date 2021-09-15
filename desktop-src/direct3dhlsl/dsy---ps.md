---
title: dsy - ps
description: Calcule la velocidad de cambio en la dirección Y del destino de representación.
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5f595d836ed8eb8525175ddb81e743cb7a04811
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573853"
---
# <a name="dsy---ps"></a>dsy - ps

Calcule la velocidad de cambio en la dirección Y del destino de representación.

## <a name="syntax"></a>Sintaxis



| dsy dst, src |
|--------------|



 

Donde:

-   dst es un registro de destino.
-   src es un registro de origen de entrada.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dsy                   |      |      |      |      |      | x    | x     | x    | x     |



 

La tasa de cambio calculada desde el registro de origen es una aproximación al contenido del mismo registro en píxeles adyacentes que ejecutan el sombreador de píxeles en el paso de bloqueo con el píxel actual.

Las [instrucciones dsx](dsx---ps.md) And dsy calculan su resultado observando el contenido actual del registro de origen (por componente) para los distintos píxeles del área local que se ejecuta en el paso de bloqueo. La fórmula exacta utilizada para calcular el degradado varía en función del hardware, pero debe ser coherente con la forma en que el hardware realiza las mismas operaciones como parte del proceso de cálculo de nivel de detalle para el muestreo de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[texldd - ps](texldd---ps.md)
</dt> </dl>

 

 




