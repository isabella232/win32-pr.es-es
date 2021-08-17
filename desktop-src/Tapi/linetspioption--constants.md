---
description: Las constantes LINETSPIOPTION \_ describen los proveedores de servicios de pedidos a los que se debe llamar.
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: LINETSPIOPTION_ constantes (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5d4a57edd80a83ab442313706fd40a2fbd79f545a0b3e9485e5d8c88b8c2f8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404865"
---
# <a name="linetspioption_-constants"></a>LineTSPIOPTION \_ (Constantes)

Las **constantes LINETSPIOPTION \_ describen** los proveedores de servicios de pedidos a los que se debe llamar.

<dl> <dt>

<span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION \_ NONREENTRANT**
</dt> <dd> <dl> <dt>



TAPI debe llamar a las funciones de este proveedor de servicios de una en una; debe esperar a que cada función devuelva (pero no a que se completen las funciones asincrónicas) antes de llamar a la misma función u otra, ya sea en el mismo subproceso o en otro, en el mismo procesador o en otro diferente.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



 

 




