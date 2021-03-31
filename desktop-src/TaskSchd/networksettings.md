---
title: Objeto NetworkSettings
description: En el caso de scripting, proporciona la configuración que el servicio Programador de tareas utiliza para obtener un perfil de red.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- Objeto NetworkSettings Programador de tareas
- Programador de tareas de objeto NetworkSettings, descrito
topic_type:
- apiref
api_name:
- NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1eecfbbdd4e3ea00c8d2412ae912594f2ec297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491093"
---
# <a name="networksettings-object"></a>Objeto NetworkSettings

En el caso de scripting, proporciona la configuración que el servicio Programador de tareas utiliza para obtener un perfil de red.

## <a name="members"></a>Miembros

El objeto **NetworkSettings** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **NetworkSettings** tiene estas propiedades.



| Propiedad                                        | Tipo de acceso           | Descripción                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Sesión**](networksettings-id.md)<br/>     | Lectura/escritura<br/> | Obtiene o establece un valor GUID que identifica un perfil de red.<br/>                        |
| [**Name**](networksettings-name.md)<br/> | Lectura/escritura<br/> | Obtiene o establece el nombre de un perfil de red. El nombre se usa para fines de presentación. <br/> |



 

## <a name="remarks"></a>Observaciones

Al leer o escribir su propio XML para una tarea, la configuración de red se especifica mediante el elemento [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Programador de tareas](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





