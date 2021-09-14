---
title: Objeto IdleSettings
description: Objeto de scripting que especifica cómo el Programador de tareas realiza tareas cuando el equipo está en una condición inactiva.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- Valor del objeto IdleSettings Programador de tareas
- Objeto IdleSettings Programador de tareas , descrito
topic_type:
- apiref
api_name:
- IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 819ff226386f30483de96fac6213b35d7dd51a52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073439"
---
# <a name="idlesettings-object"></a>Objeto IdleSettings

Objeto de scripting que especifica cómo el Programador de tareas realiza tareas cuando el equipo está en una condición de inactividad. Para obtener información sobre las condiciones de inactividad, vea [Task Idle Conditions](task-idle-conditions.md).

## <a name="members"></a>Members

El **objeto IdleSettings** tiene estos tipos de miembros:

- [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto IdleSettings** tiene estas propiedades.

> [!NOTE]
> Las *opciones IdleDuration* *y WaitTimeout* están en desuso. Todavía están presentes en la interfaz de usuario Programador de tareas y sus métodos de interfaz pueden devolver valores válidos, pero ya no se usan.

| Propiedad.                                                       | Tipo de acceso           | Descripción                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](idlesettings-restartonidle.md)<br/> | Lectura y escritura<br/> | Obtiene o establece un valor booleano que indica si la tarea se reinicia cuando el equipo pasa a una condición de inactividad más de una vez.<br/>            |
| [**StopOnIdleEnd**](idlesettings-stoponidleend.md)<br/> | Lectura y escritura<br/> | Obtiene o establece un valor booleano que indica que el Programador de tareas finalizará la tarea si la condición de inactividad finaliza antes de que se complete la tarea.<br/> |
| **En desuso:** [ **IdleDuration**](idlesettings-idleduration.md)<br/>   | Lectura y escritura<br/> | Obtiene o establece un valor que indica la cantidad de tiempo que el equipo debe estar en estado inactivo antes de ejecutar la tarea.<br/>                            |
| **En desuso:** [ **WaitTimeout**](idlesettings-waittimeout.md)<br/>     | Lectura y escritura<br/> | Obtiene o establece un valor que indica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad.<br/>                             |

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) del Programador de tareas esquema.

Si un desencadenador inactivo desencadena una tarea, se omite la propiedad [**IdleSettings.WaitTimeout.**](idlesettings-waittimeout.md)

> [!NOTE]
> *IdleSettings.IdleDuration* e *IdleSettings.WaitTimeout están en* desuso.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |

## <a name="see-also"></a>Vea también

[Programador de tareas objetos](task-scheduler-objects.md)

[Programador de tareas](task-scheduler-start-page.md)
