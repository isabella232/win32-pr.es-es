---
description: Las constantes LINEAGENTSTATE \_ describen el estado de un agente en una dirección.
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: LINEAGENTSTATE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001b760a5b566089814195b11fc39dc356a3444f5c5dc6ee26e71a471e26e338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140118"
---
# <a name="lineagentstate_-constants"></a>Constantes \_ LINEAGENTSTATE

Las **constantes LINEAGENTSTATE \_** describen el estado de un agente en una dirección.

<dl> <dt>

<span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE \_ BUSYACD**
</dt> <dd> <dl> <dt>



El agente está ocupado controlando una llamada enrutada desde una cola de ACD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE \_ BUSYINCOMING**
</dt> <dd> <dl> <dt>



El agente está ocupado controlando una llamada entrante que no se ha transferido al agente desde una cola de ACD en la que el agente ha iniciado sesión.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE \_ BUSYOTHER**
</dt> <dd> <dl> <dt>



El agente está ocupado controlando otro tipo de llamada, como una llamada personal saliente no transferida al agente por un marcador predictivo. Este valor también se puede usar cuando se sabe que el agente está ocupado en una llamada, pero se desconoce el tipo de llamada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE \_ BUSYOUTBOUND**
</dt> <dd> <dl> <dt>



El agente está ocupado controlando una llamada saliente, como una enrutada desde una cola de marcado predictivo.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE \_ LOGGEDOFF**
</dt> <dd> <dl> <dt>



Ningún agente ha iniciado sesión en la dirección.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE \_ NOTREADY**
</dt> <dd> <dl> <dt>



El agente ha iniciado sesión, pero está ocupado con una tarea que no sea atender una llamada (por ejemplo, en una interrupción). No se debe enrutar ninguna llamada adicional al agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE \_ READY**
</dt> <dd> <dl> <dt>



El agente está listo para aceptar llamadas.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



El estado del agente es desconocido y nunca se conocerá. En [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), esta condición también se puede representar mediante el **miembro dwAgentState** que se establece en 0.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



El estado del agente es desconocido actualmente, pero puede conocerse más adelante. Puede ser un estado transitorio cuando se abre por primera vez una línea o una dirección.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE \_ WORKINGAFTERCALL**
</dt> <dd> <dl> <dt>



El agente ha completado la llamada anterior, pero sigue ocupado por el trabajo relacionado con esa llamada. El agente no debe recibir llamadas adicionales.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Los 16 bits superiores de este conjunto de constantes están reservados para extensiones específicas del dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




