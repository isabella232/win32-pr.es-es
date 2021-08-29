---
title: dsx - ps
description: Calcule la velocidad de cambio en la dirección X del destino de representación.
ms.assetid: 3358ddca-97a3-421d-8e5d-6b425903e683
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 41307f89b4fe47276917cacb4bc5208388060feac4e63aacb4046abe87f00554
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673775"
---
# <a name="dsx---ps"></a>dsx - ps

Calcule la velocidad de cambio en la dirección X del destino de representación.

## <a name="syntax"></a>Syntax



| dsx dst, src |
|--------------|



 

Donde:

-   dst es un registro de destino.
-   src es un registro de origen de entrada.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Dsx                   |      |      |      |      |      | x    | x     | x    | x     |



 

La tasa de cambio calculada desde el registro de origen es una aproximación al contenido del mismo registro en píxeles adyacentes que ejecutan el sombreador de píxeles en el paso de bloqueo con el píxel actual.

Las instrucciones dsx And [dsy](dsy---ps.md) calculan su resultado observando el contenido actual del registro de origen (por componente) para los distintos píxeles del área local que se ejecuta en el paso de bloqueo. La fórmula exacta usada para calcular el degradado varía en función del hardware, pero debe ser coherente con la forma en que el hardware realiza las mismas operaciones como parte del proceso de cálculo de nivel de detalle para el muestreo de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[ldd- ps](texldd---ps.md)
</dt> </dl>

 

 




