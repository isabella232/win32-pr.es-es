---
title: Objeto principal
description: Objeto de scripting que proporciona las credenciales de seguridad para una entidad de seguridad.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Objeto principal Programador de tareas
- Objeto principal Programador de tareas , descrito
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6dc9ff69973fb340bf3b140462c4012499680ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173022"
---
# <a name="principal-object"></a>Objeto principal

Objeto de scripting que proporciona las credenciales de seguridad para una entidad de seguridad. Estas credenciales de seguridad definen el contexto de seguridad para las tareas asociadas a la entidad de seguridad.

## <a name="members"></a>Members

El **objeto Principal** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Principal** tiene estas propiedades.



| Propiedad                                                | Tipo de acceso           | Descripción                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Displayname**](principal-displayname.md)<br/> | Lectura y escritura<br/> | Obtiene o establece el nombre de la entidad de seguridad que se muestra en la interfaz Programador de tareas usuario.<br/>                                                                |
| [**Groupid**](principal-groupid.md)<br/>         | Lectura y escritura<br/> | Obtiene o establece el identificador del grupo de usuarios necesario para ejecutar las tareas asociadas a la entidad de seguridad.<br/>                           |
| [**Id**](principal-id.md)<br/>                   | Lectura y escritura<br/> | Obtiene o establece el identificador de la entidad de seguridad.<br/>                                                                                                     |
| [**LogonType**](principal-logontype.md)<br/>     | Lectura y escritura<br/> | Obtiene o establece el método de inicio de sesión de seguridad necesario para ejecutar las tareas asociadas a la entidad de seguridad.<br/>                                  |
| [**Ejecución**](principal-runlevel.md)<br/>       | Lectura y escritura<br/> | Obtiene o establece el identificador que se usa para especificar el nivel de privilegios necesario para ejecutar las tareas asociadas a la entidad de seguridad.<br/> |
| [**UserId**](principal-userid.md)<br/>           | Lectura y escritura<br/> | Obtiene o establece el identificador de usuario necesario para ejecutar las tareas asociadas a la entidad de seguridad.<br/>                                        |



 

## <a name="remarks"></a>Observaciones

Al especificar una cuenta, recuerde usar correctamente la doble barra diagonal inversa en el código para especificar el dominio y el nombre de usuario. Por ejemplo, use DOMAIN \\ \\ UserName para especificar un valor para la [**propiedad UserId.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid)

Al leer o escribir XML para una tarea, las credenciales de seguridad de una entidad de seguridad se especifican en el elemento [**Principal**](taskschedulerschema-principal-principaltype-element.md) del Programador de tareas esquema.

Si una tarea se registra mediante la herramienta de línea de comandos de at.exe y este objeto se usa para recuperar información sobre la tarea, la propiedad [**LogonType**](principal-logontype.md) devolverá 0, la propiedad [**RunLevel**](principal-runlevel.md) devolverá 0 y la [**propiedad UserId**](principal-userid.md) devolverá Nothing.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea [Ejemplo de desencadenador de tiempo (scripting).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





