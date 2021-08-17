---
description: Las constantes LINEAGENTSTATEEX \_ describen el estado de un agente en una dirección.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: LINEAGENTSTATEEX_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f46c00b337a9106165616fe2eaf86bd2b2634b0c113369558953203313d59f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140098"
---
# <a name="lineagentstateex_-constants"></a>Constantes LINEAGENTSTATEEX \_

Las **constantes LINEAGENTSTATEEX \_ describen** el estado de un agente en una dirección.

<dl> <dt>

<span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX \_ BUSYACD**
</dt> <dd> <dl> <dt>



El agente está ocupado controlando una llamada enrutada desde una cola de ACD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX \_ BUSYINCOMING**
</dt> <dd> <dl> <dt>



El agente está ocupado controlando una llamada entrante que no se ha transferido al agente desde una cola de ACD en la que el agente ha iniciado sesión.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX \_ BUSYOUTGOING**
</dt> <dd> <dl> <dt>



El agente está ocupado controlando una llamada saliente, como una enrutada desde una cola de marcado predictivo.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ NOTREADY**
</dt> <dd> <dl> <dt>



El agente ha iniciado sesión, pero está ocupado con una tarea que no sea atender una llamada (por ejemplo, en una interrupción). No se debe enrutar ninguna llamada adicional al agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ READY**
</dt> <dd> <dl> <dt>



El agente está listo para aceptar llamadas.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX \_ PUBLICADO**
</dt> <dd> <dl> <dt>



El agente se ha liberado, probablemente porque ha cerrado sesión.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ UNKNOWN**
</dt> <dd> <dl> <dt>



El estado del agente es desconocido actualmente, pero puede conocerse más adelante. Puede ser un estado transitorio cuando se abre por primera vez una línea o una dirección.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




