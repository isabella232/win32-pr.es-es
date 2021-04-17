---
description: Las \_ constantes LINEAGENTSTATEEX describen el estado de un agente en una dirección.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: Constantes de LINEAGENTSTATEEX_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 214b816a35e3fdb420a9d95772c466791c6d2f2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690973"
---
# <a name="lineagentstateex_-constants"></a>Constantes de LINEAGENTSTATEEX \_

Las **\_ constantes LINEAGENTSTATEEX** describen el estado de un agente en una dirección.

<dl> <dt>

<span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX \_ BUSYACD**
</dt> <dd> <dl> <dt>



El agente está ocupado administrando una llamada enrutada desde una cola de ACD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX \_ BUSYINCOMING**
</dt> <dd> <dl> <dt>



El agente está ocupado administrando una llamada entrante que no se transfirió al agente desde una cola de ACD en la que el agente ha iniciado sesión.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX \_ BUSYOUTGOING**
</dt> <dd> <dl> <dt>



El agente está ocupado administrando una llamada saliente, como una enrutada desde una cola de marcado predictivo.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ NOhuellal**
</dt> <dd> <dl> <dt>



El agente ha iniciado sesión, pero está ocupado con una tarea que no es atender una llamada (por ejemplo, en un salto). No se deben enrutar llamadas adicionales al agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ listo**
</dt> <dd> <dl> <dt>



El agente está listo para aceptar llamadas.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX \_ liberado**
</dt> <dd> <dl> <dt>



El agente se ha liberado, probablemente porque ha cerrado la sesión.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ desconocido**
</dt> <dd> <dl> <dt>



El estado del agente es desconocido actualmente, pero puede ser conocido más adelante. Puede ser un estado de transición cuando se abre por primera vez una línea o dirección.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,2<br/>                                                      |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




