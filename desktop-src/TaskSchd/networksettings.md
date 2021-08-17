---
title: Objeto NetworkSettings
description: Para el scripting, proporciona la configuración que el Programador de tareas utiliza para obtener un perfil de red.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- Objeto NetworkSettings Programador de tareas
- Objeto NetworkSettings Programador de tareas , descrito
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
ms.openlocfilehash: ddc5e247ad3de50268c6075f8956687f92800c4e901788b5098a0cef868bb202
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759697"
---
# <a name="networksettings-object"></a>Objeto NetworkSettings

Para el scripting, proporciona la configuración que el Programador de tareas utiliza para obtener un perfil de red.

## <a name="members"></a>Miembros

El **objeto NetworkSettings** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto NetworkSettings** tiene estas propiedades.



| Propiedad                                        | Tipo de acceso           | Descripción                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Id**](networksettings-id.md)<br/>     | Lectura/escritura<br/> | Obtiene o establece un valor GUID que identifica un perfil de red.<br/>                        |
| [**Nombre**](networksettings-name.md)<br/> | Lectura/escritura<br/> | Obtiene o establece el nombre de un perfil de red. El nombre se usa con fines para mostrar. <br/> |



 

## <a name="remarks"></a>Comentarios

Al leer o escribir su propio XML para una tarea, la configuración de red se especifica mediante el [**elemento NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas objetos](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





