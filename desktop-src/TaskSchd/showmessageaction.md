---
title: Objeto ShowMessageAction
description: En el caso de scripting, representa una acción que muestra un cuadro de mensaje cuando se activa una tarea.
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- Objeto ShowMessageAction Programador de tareas
- Programador de tareas de objeto ShowMessageAction, descrito
topic_type:
- apiref
api_name:
- ShowMessageAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1e500f0492ad010e88719a467fda38f85e184c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422099"
---
# <a name="showmessageaction-object"></a>Objeto ShowMessageAction

\[Este objeto ya no se admite. Puede usar IExecAction con la [**función MsgBox**](/previous-versions/sfw6660x(v=vs.80)) de scripting de Windows para mostrar un mensaje en la sesión de usuario.\]

En el caso de scripting, representa una acción que muestra un cuadro de mensaje cuando se activa una tarea.

## <a name="members"></a>Miembros

El objeto **ShowMessageAction** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **ShowMessageAction** tiene estas propiedades.



| Propiedad                                                        | Tipo de acceso           | Descripción                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Sesión**](action-id.md)<br/>                              | Lectura/escritura<br/> | Heredado del objeto de [**acción**](action.md) . Obtiene o establece el identificador de la acción.<br/> |
| [**MessageBody**](showmessageaction-messagebody.md)<br/> | Lectura/escritura<br/> | Obtiene o establece el texto del mensaje que se muestra en el cuerpo del cuadro de mensaje.<br/>                |
| [**Title**](showmessageaction-title.md)<br/>             | Lectura/escritura<br/> | Obtiene o establece el título del cuadro de mensaje.<br/>                                                     |
| [**Tipo**](action-type.md)<br/>                          | Solo lectura<br/>  | Heredado del objeto de [**acción**](action.md) . Obtiene el tipo de la acción.<br/>               |



 

## <a name="remarks"></a>Observaciones

En el caso de una tarea que contenga una acción de cuadro de mensaje, se mostrará el cuadro de mensaje si la tarea está activada y la tarea tiene un tipo de inicio de sesión interactivo. Para establecer el tipo de inicio de sesión de tarea en interactivo, especifique 3 (**\_ \_ \_ token interactivo de inicio de sesión de tarea**) o 4 (**\_ \_ grupo de inicio de sesión de tareas**) en la propiedad [**LogonType**](principal-logontype.md) de la entidad de seguridad de la tarea, o en el parámetro *LogonType* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

Al leer o escribir su propio XML para una tarea, se especifica una acción de cuadro de mensaje mediante el elemento [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) del esquema de programador de tareas.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de cuadro de mensaje (scripting)](/previous-versions//aa381916(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                    |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

