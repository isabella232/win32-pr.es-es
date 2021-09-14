---
title: Método TriggerCollection.Create
description: Para el scripting, crea un nuevo desencadenador para la tarea.
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- desencadenadores Programador de tareas , creando
- Creación de un método Programador de tareas
- Crear método Programador de tareas , objeto TriggerCollection
- TriggerCollection object Programador de tareas , Create method
topic_type:
- apiref
api_name:
- TriggerCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0f1c5dd8bef3d81a8e9b5859bc2bbd8c969bf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891385"
---
# <a name="triggercollectioncreate-method"></a>Método TriggerCollection.Create

Para el scripting, crea un nuevo desencadenador para la tarea.

## <a name="syntax"></a>Sintaxis


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*type* \[ En\]
</dt> <dd>

Este parámetro se establece en una de las siguientes constantes de enumeración [**TASK \_ TRIGGER \_ TYPE2.**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)



| Value                                                                                                                                                                                                                                                                                | Significado                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**TASK \_ TRIGGER \_ EVENT**</dt> <dt>0</dt> </dl>                                                 | Desencadena la tarea cuando se produce un evento específico.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**TASK \_ TIEMPO \_ DE DESENCADENADOR**</dt> <dt>1</dt> </dl>                                                    | Desencadena la tarea a una hora específica del día.<br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**TASK \_ DESENCADENADOR \_ DIARIO**</dt> <dt>2</dt> </dl>                                                 | Desencadena la tarea según una programación diaria. Por ejemplo, la tarea se inicia a una hora específica cada día, cada otro día, cada tercer día, y así sucesivamente.<br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**TASK \_ TRIGGER \_ WEEKLY**</dt> <dt>3</dt> </dl>                                              | Desencadena la tarea según una programación semanal. Por ejemplo, la tarea se inicia a las 8:00 a. m. en un día específico cada semana u otra semana.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**TASK \_ DESENCADENADOR \_ MENSUAL**</dt> <dt>4</dt> </dl>                                           | Desencadena la tarea según una programación mensual. Por ejemplo, la tarea se inicia en días específicos de meses específicos.<br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**TASK \_ TRIGGER \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Desencadena la tarea según una programación mensual del día de la semana. Por ejemplo, la tarea se inicia en días específicos de la semana, semanas del mes y meses del año.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**TASK \_ DESENCADENADOR \_ INACTIVO**</dt> <dt>6</dt> </dl>                                                    | Desencadena la tarea cuando el equipo entra en estado inactivo.<br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**TASK \_ REGISTRO \_ DE DESENCADENADOR**</dt> <dt>7</dt> </dl>                            | Desencadena la tarea cuando se registra la tarea.<br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**TASK \_ TRIGGER \_ BOOT**</dt> <dt>8</dt> </dl>                                                    | Desencadena la tarea cuando se inicia el equipo.<br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**TASK \_ DESENCADENAR \_ INICIO DE SESIÓN**</dt> <dt>9</dt> </dl>                                                 | Desencadena la tarea cuando un usuario específico inicia sesión.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**TASK \_ TRIGGER SESSION STATE CHANGE 11 (DESENCADENAR CAMBIO \_ \_ DE ESTADO DE \_ SESIÓN**</dt> <dt>11)</dt> </dl> | Desencadena la tarea cuando cambia un estado de sesión específico.<br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**Trigger**](trigger.md) que representa el nuevo desencadenador.

## <a name="remarks"></a>Observaciones

Para obtener información sobre cada tipo de desencadenador, vea [Tipos de desencadenador.](trigger-types.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**Detonante**](trigger.md)
</dt> </dl>

 

 





