---
description: Las \_ constantes LINEAGENTSTATE describen el estado de un agente en una dirección.
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: Constantes de LINEAGENTSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b5afa8f93cfde5529f8f57fd8e48d37ecd415b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681097"
---
# <a name="lineagentstate_-constants"></a>Constantes de LINEAGENTSTATE \_

Las **\_ constantes LINEAGENTSTATE** describen el estado de un agente en una dirección.

<dl> <dt>

<span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE \_ BUSYACD**
</dt> <dd> <dl> <dt>



El agente está ocupado administrando una llamada enrutada desde una cola de ACD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE \_ BUSYINCOMING**
</dt> <dd> <dl> <dt>



El agente está ocupado administrando una llamada entrante que no se transfirió al agente desde una cola de ACD en la que el agente ha iniciado sesión.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE \_ BUSYOTHER**
</dt> <dd> <dl> <dt>



El agente está ocupado administrando otro tipo de llamada, como una llamada personal de salida que no se transfiere al agente mediante un marcador de predicción. Este valor también se puede usar cuando se sabe que el agente está ocupado en una llamada, pero se desconoce el tipo de llamada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE \_ BUSYOUTBOUND**
</dt> <dd> <dl> <dt>



El agente está ocupado administrando una llamada saliente, como una enrutada desde una cola de marcado predictivo.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE \_ LOGGEDOFF**
</dt> <dd> <dl> <dt>



Ningún agente ha iniciado sesión en la dirección.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE \_ NOhuellal**
</dt> <dd> <dl> <dt>



El agente ha iniciado sesión, pero está ocupado con una tarea que no es atender una llamada (por ejemplo, en un salto). No se deben enrutar llamadas adicionales al agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE \_ listo**
</dt> <dd> <dl> <dt>



El agente está listo para aceptar llamadas.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE no \_ disponible**
</dt> <dd> <dl> <dt>



El estado del agente es desconocido y nunca se conocerá. En [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), esta condición también se puede representar mediante el miembro **dwAgentState** que se establece en 0.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE \_ desconocido**
</dt> <dd> <dl> <dt>



El estado del agente es desconocido actualmente, pero puede ser conocido más adelante. Puede ser un estado de transición cuando se abre por primera vez una línea o dirección.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE \_ WORKINGAFTERCALL**
</dt> <dd> <dl> <dt>



El agente ha completado la llamada anterior, pero sigue ocupado con el trabajo relacionado con esa llamada. El agente no debe recibir llamadas adicionales.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los 16 bits superiores de este conjunto de constantes se reservan para las extensiones específicas del dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




