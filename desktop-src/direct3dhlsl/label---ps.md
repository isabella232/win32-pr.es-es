---
title: 'label: ps'
description: 'Marque la siguiente instrucción como si tiene un índice de etiqueta. | label: ps'
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3fb266b649642c82293e8310b6302c6763ddc27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568356"
---
# <a name="label---ps"></a>label: ps

Marque la siguiente instrucción como si tiene un índice de etiqueta.

## <a name="syntax"></a>Sintaxis



| etiqueta l\# |
|-----------|



 

donde \# identifica el número de etiqueta.

Para ps \_ 2 \_ x, el número de etiqueta debe estar entre 0 y 15.

Para ps 2 sw, ps 3 0 y ps 3 sw, el número de etiqueta debe estar entre \_ \_ \_ \_ \_ \_ 0 y 2047.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| etiqueta                 |      |      |      |      |      | x    | x     | x    | x     |



 

Esta instrucción define una etiqueta ubicada en la siguiente instrucción del sombreador. La instrucción de etiqueta solo puede estar presente directamente después de una [instrucción ret](ret---ps.md) (que define el final de la subrutina anterior o el programa principal).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




