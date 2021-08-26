---
title: Interfaz IRDVTaskPluginNotifySink
description: El agente de tareas usa la interfaz IRDVTaskPluginNotifySink para comunicarse con el agente desencadenador.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- Interfaz IRDVTaskPluginNotifySink Servicios de Escritorio remoto
- Interfaz IRDVTaskPluginNotifySink Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88692175fedbad4faf5b2755ce92897cff25fe9d588e6fb446d8174407aa6b5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072395"
---
# <a name="irdvtaskpluginnotifysink-interface"></a>Interfaz IRDVTaskPluginNotifySink

El agente de tareas usa la interfaz **IRDVTaskPluginNotifySink** para comunicarse con el agente desencadenador. Se pasa un puntero a esta interfaz al agente de tareas en el [**método IRDVTaskPlugin::Initialize.**](irdvtaskplugin-initialize.md)

## <a name="members"></a>Miembros

La **interfaz IRDVTaskPluginNotifySink** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IRDVTaskPluginNotifySink** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IRDVTaskPluginNotifySink** tiene estos métodos.



| Método                                                                  | Descripción                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**DeleteSchedule**](irdvtaskpluginnotifysink-deleteschedule.md)       | Llamado por el agente de tareas para eliminar una tarea programada.<br/>                   |
| [**OnTaskStateChange**](irdvtaskpluginnotifysink-ontaskstatechange.md) | Se usa para notificar al agente de desencadenador que el estado de una tarea ha cambiado.<br/> |
| [**OnTerminated**](irdvtaskpluginnotifysink-onterminated.md)           | Llamado por el agente de tareas para solicitar que se cierre el agente de tareas.<br/>  |
| [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md)           | Llamado por el agente de tareas para programar una tarea.<br/>                           |



 

## <a name="remarks"></a>Comentarios

Aunque esta interfaz se admite en los sistemas operativos identificados en los siguientes requisitos, solo se usará si la máquina virtual se hospeda en Windows Server 2012.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



 

