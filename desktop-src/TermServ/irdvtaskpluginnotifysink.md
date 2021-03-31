---
title: Interfaz IRDVTaskPluginNotifySink
description: El agente de tareas usa la interfaz IRDVTaskPluginNotifySink para comunicarse con el agente desencadenador.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IRDVTaskPluginNotifySink
- Servicios de Escritorio remoto de la interfaz IRDVTaskPluginNotifySink, descrito
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0dadaf387fcf6e8381404440e0d31dd210b9f8a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802702"
---
# <a name="irdvtaskpluginnotifysink-interface"></a>Interfaz IRDVTaskPluginNotifySink

El agente de tareas usa la interfaz **IRDVTaskPluginNotifySink** para comunicarse con el agente desencadenador. Un puntero a esta interfaz se pasa al agente de tarea en el método [**IRDVTaskPlugin:: Initialize**](irdvtaskplugin-initialize.md) .

## <a name="members"></a>Miembros

La interfaz **IRDVTaskPluginNotifySink** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRDVTaskPluginNotifySink** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IRDVTaskPluginNotifySink** tiene estos métodos.



| Método                                                                  | Descripción                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**DeleteSchedule**](irdvtaskpluginnotifysink-deleteschedule.md)       | El agente de tareas lo llama para eliminar una tarea programada.<br/>                   |
| [**OnTaskStateChange**](irdvtaskpluginnotifysink-ontaskstatechange.md) | Se usa para notificar al agente de desencadenador que el estado de una tarea ha cambiado.<br/> |
| [**Terminado**](irdvtaskpluginnotifysink-onterminated.md)           | El agente de tareas lo llama para solicitar que se cierre el agente de tareas.<br/>  |
| [**ScheduleTask (**](irdvtaskpluginnotifysink-scheduletask.md)           | Llamado por el agente de tareas para programar una tarea.<br/>                           |



 

## <a name="remarks"></a>Observaciones

Aunque esta interfaz es compatible con los sistemas operativos identificados en los requisitos siguientes, solo se usará si la máquina virtual está hospedada en Windows Server 2012.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



 

