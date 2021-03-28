---
title: etiqueta-PS
description: Marque la instrucción siguiente como un índice de etiqueta. | etiqueta-PS
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3fb266b649642c82293e8310b6302c6763ddc27
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998156"
---
# <a name="label---ps"></a>etiqueta-PS

Marque la instrucción siguiente como un índice de etiqueta.

## <a name="syntax"></a>Sintaxis



| etiqueta l\# |
|-----------|



 

donde \# identifica el número de etiqueta.

Para PS \_ 2 \_ x, el número de etiqueta debe estar entre 0 y 15.

Para PS \_ 2 \_ SW, PS \_ 3 \_ 0 y PS \_ 3 \_ SW, el número de etiqueta debe estar entre 0 y 2047.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| etiqueta                 |      |      |      |      |      | x    | x     | x    | x     |



 

Esta instrucción define una etiqueta que se encuentra en la siguiente instrucción del sombreador. La instrucción de etiqueta solo puede estar presente directamente después de una instrucción [RET](ret---ps.md) (que define el final de la subrutina o el programa principal anterior).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




