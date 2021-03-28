---
title: llamada a PS
description: Realiza una llamada de función a la instrucción marcada con la etiqueta proporcionada. | llamada a PS
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27be29c478afdf92c29fefd16a82319e0899d2ec
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998113"
---
# <a name="call---ps"></a>llamada a PS

Realiza una llamada de función a la instrucción marcada con la etiqueta proporcionada.

## <a name="syntax"></a>Sintaxis



| llamar a l\# |
|----------|



 

Donde:

-   l \# es una [etiqueta-PS](label---ps.md) que marca el principio de la subrutina a la que se va a llamar.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| llamada                  |      |      |      |      |      | x    | x     | x    | x     |



 

Esta instrucción hace lo siguiente:

1.  Dirección de extracción de la instrucción siguiente a la pila de direcciones devuelta.
2.  Continúe con la ejecución de la instrucción marcada por la etiqueta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




