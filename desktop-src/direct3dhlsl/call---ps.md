---
title: call - ps
description: Realiza una llamada de función a la instrucción marcada con la etiqueta proporcionada. | call - ps
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27be29c478afdf92c29fefd16a82319e0899d2ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574013"
---
# <a name="call---ps"></a>call - ps

Realiza una llamada de función a la instrucción marcada con la etiqueta proporcionada.

## <a name="syntax"></a>Sintaxis



| llamar a l\# |
|----------|



 

Donde:

-   l \# es una [etiqueta: ps](label---ps.md) que marca el principio de la subrutina a la que se va a llamar.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| llamada                  |      |      |      |      |      | x    | x     | x    | x     |



 

Esta instrucción hace lo siguiente:

1.  Dirección de inserción de la siguiente instrucción en la pila de direcciones de retorno.
2.  Continúe la ejecución desde la instrucción marcada por la etiqueta .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




