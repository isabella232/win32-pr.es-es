---
title: Objeto principal
description: Objeto de scripting que proporciona las credenciales de seguridad para una entidad de seguridad.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Programador de tareas de objeto principal
- Programador de tareas de objeto principal, descrito
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905120"
---
# <a name="principal-object"></a>Objeto principal

Objeto de scripting que proporciona las credenciales de seguridad para una entidad de seguridad. Estas credenciales de seguridad definen el contexto de seguridad para las tareas que están asociadas a la entidad de seguridad.

## <a name="members"></a>Miembros

El objeto **principal** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto de **entidad** de seguridad tiene estas propiedades.



| Propiedad                                                | Tipo de acceso           | Descripción                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](principal-displayname.md)<br/> | Lectura/escritura<br/> | Obtiene o establece el nombre de la entidad de seguridad que se muestra en la interfaz de usuario de Programador de tareas.<br/>                                                                |
| [**GroupId**](principal-groupid.md)<br/>         | Lectura/escritura<br/> | Obtiene o establece el identificador del grupo de usuarios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.<br/>                           |
| [**Sesión**](principal-id.md)<br/>                   | Lectura/escritura<br/> | Obtiene o establece el identificador de la entidad de seguridad.<br/>                                                                                                     |
| [**LogonType**](principal-logontype.md)<br/>     | Lectura/escritura<br/> | Obtiene o establece el método de inicio de sesión de seguridad necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.<br/>                                  |
| [**Nivel**](principal-runlevel.md)<br/>       | Lectura/escritura<br/> | Obtiene o establece el identificador que se usa para especificar el nivel de privilegios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.<br/> |
| [**Deberían**](principal-userid.md)<br/>           | Lectura/escritura<br/> | Obtiene o establece el identificador de usuario necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.<br/>                                        |



 

## <a name="remarks"></a>Observaciones

Al especificar una cuenta, no olvide usar correctamente la doble barra diagonal inversa en el código para especificar el dominio y el nombre de usuario. Por ejemplo, use \\ \\ el nombre de usuario de dominio para especificar un valor para la propiedad [**userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .

Al leer o escribir XML para una tarea, las credenciales de seguridad de una entidad de seguridad se especifican en el elemento [**principal**](taskschedulerschema-principal-principaltype-element.md) del esquema de programador de tareas.

Si una tarea se registra con la herramienta de línea de comandos at.exe y este objeto se usa para recuperar información sobre la tarea, la propiedad [**LogonType**](principal-logontype.md) devolverá 0, la propiedad [**nivel**](principal-runlevel.md) devolverá 0 y la propiedad [**userid**](principal-userid.md) no devolverá nada.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





