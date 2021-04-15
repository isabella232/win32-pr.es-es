---
title: Objeto IdleSettings
description: Objeto de scripting que especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en una condición de inactividad.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- Objeto IdleSettings Programador de tareas
- Programador de tareas de objeto IdleSettings, descrito
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422167"
---
# <a name="idlesettings-object"></a>Objeto IdleSettings

Objeto de scripting que especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en una condición de inactividad. Para obtener información sobre las condiciones de inactividad, consulte [condiciones de inactividad de tareas](task-idle-conditions.md).

## <a name="members"></a>Miembros

El objeto **IdleSettings** tiene estos tipos de miembros:

- [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **IdleSettings** tiene estas propiedades.

> [!NOTE]
> La configuración de *IdleDuration* y *WaitTimeout* está en desuso. Todavía están presentes en la interfaz de usuario de Programador de tareas y sus métodos de interfaz todavía pueden devolver valores válidos, pero ya no se usan.

| Propiedad                                                       | Tipo de acceso           | Descripción                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](idlesettings-restartonidle.md)<br/> | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica si la tarea se reinicia cuando el equipo se recorre en una condición de inactividad más de una vez.<br/>            |
| [**StopOnIdleEnd**](idlesettings-stoponidleend.md)<br/> | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que el Programador de tareas finalizará la tarea si la condición de inactividad finaliza antes de que se complete la tarea.<br/> |
| En **desuso**: [ **IdleDuration**](idlesettings-idleduration.md)<br/>   | Lectura/escritura<br/> | Obtiene o establece un valor que indica la cantidad de tiempo que el equipo debe estar en un estado de inactividad antes de que se ejecute la tarea.<br/>                            |
| En **desuso**: [ **WaitTimeout**](idlesettings-waittimeout.md)<br/>     | Lectura/escritura<br/> | Obtiene o establece un valor que indica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad.<br/>                             |

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) del esquema de programador de tareas.

Si una tarea se desencadena mediante un desencadenador inactivo, se omite la propiedad [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) .

> [!NOTE]
> *IdleSettings. IdleDuration* y *IdleSettings. WaitTimeout* están desusados.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |

## <a name="see-also"></a>Vea también

[Objetos Programador de tareas](task-scheduler-objects.md)

[Programador de tareas](task-scheduler-start-page.md)
