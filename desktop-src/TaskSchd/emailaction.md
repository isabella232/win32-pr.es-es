---
title: Objeto EmailAction
description: Objeto de scripting que representa una acción que envía un mensaje de correo electrónico.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- Objeto EmailAction Programador de tareas
- Programador de tareas de objeto EmailAction, descrito
topic_type:
- apiref
api_name:
- EmailAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a339a1549b76f61499b7192a48edc7c1b86a6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905536"
---
# <a name="emailaction-object"></a>Objeto EmailAction

\[Este objeto ya no se admite. Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.\]

Objeto de scripting que representa una acción que envía un mensaje de correo electrónico.

## <a name="members"></a>Miembros

El objeto **EmailAction** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **EmailAction** tiene estas propiedades.



| Propiedad                                                    | Tipo de acceso           | Descripción                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Datos adjuntos**](emailaction-attachments.md)<br/>   | Lectura/escritura<br/> | Obtiene o establece una matriz de datos adjuntos que se envía con el mensaje de correo electrónico.<br/>                      |
| [**CCO**](emailaction-bcc.md)<br/>                   | Lectura/escritura<br/> | Obtiene o establece la dirección o direcciones de correo electrónico que se van a incluir en el mensaje de correo electrónico.<br/>         |
| [**Cuerpo**](emailaction-body.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece el cuerpo del correo electrónico que contiene el mensaje de correo electrónico.<br/>                            |
| [**Correos**](emailaction-cc.md)<br/>                     | Lectura/escritura<br/> | Obtiene o establece la dirección o direcciones de correo electrónico que desea CC en el mensaje de correo electrónico.<br/>          |
| [**From**](emailaction-from.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece la dirección de correo electrónico de la que desea enviar el correo electrónico.<br/>                           |
| [**HeaderFields**](emailaction-headerfields.md)<br/> | Lectura/escritura<br/> | Obtiene o establece la información de encabezado del correo electrónico que se desea enviar.<br/>                        |
| [**Sesión**](action-id.md)<br/>                          | Lectura/escritura<br/> | Heredado del objeto de [**acción**](action.md) . Obtiene o establece el identificador de la acción.<br/> |
| [**ReplyTo**](emailaction-replyto.md)<br/>           | Lectura/escritura<br/> | Obtiene o establece la dirección de correo electrónico a la que se desea responder.<br/>                                      |
| [**Server**](emailaction-server.md)<br/>             | Lectura/escritura<br/> | Obtiene o establece el nombre del servidor del que se usa para enviar correo electrónico.<br/>                           |
| [**Asunto**](emailaction-subject.md)<br/>           | Lectura/escritura<br/> | Obtiene o establece el asunto del mensaje de correo electrónico.<br/>                                                 |
| [**En**](emailaction-to.md)<br/>                     | Lectura/escritura<br/> | Obtiene o establece las direcciones de correo electrónico a las que desea enviar el correo electrónico.<br/>                |
| [**Tipo**](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | Solo lectura<br/>  | Heredado del objeto de [**acción**](action.md) . Obtiene el tipo de la acción.<br/>                   |



 

## <a name="remarks"></a>Observaciones

La acción de correo electrónico debe tener un valor válido para las propiedades [**Server**](emailaction-server.md), [**from**](emailaction-from.md)y [**to**](emailaction-to.md) o [**CC**](emailaction-cc.md) para que la tarea se registre y se ejecute correctamente.

Al leer o escribir su propio XML para una tarea, se especifica una acción de correo electrónico mediante el elemento [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) del esquema de programador de tareas.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de eventos (scripting)](/previous-versions//aa446887(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                    |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

