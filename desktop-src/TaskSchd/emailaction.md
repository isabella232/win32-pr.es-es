---
title: Objeto EmailAction
description: Objeto de scripting que representa una acción que envía un mensaje de correo electrónico.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- Objeto EmailAction Programador de tareas
- Objeto EmailAction Programador de tareas , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068668"
---
# <a name="emailaction-object"></a>Objeto EmailAction

\[Este objeto ya no se admite. Use IExecAction con el cmdlet [**Send-MailMessage de**](/powershell/module/microsoft.powershell.utility/send-mailmessage) PowerShell como solución alternativa.\]

Objeto de scripting que representa una acción que envía un mensaje de correo electrónico.

## <a name="members"></a>Members

El **objeto EmailAction** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto EmailAction** tiene estas propiedades.



| Propiedad                                                    | Tipo de acceso           | Descripción                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Datos adjuntos**](emailaction-attachments.md)<br/>   | Lectura y escritura<br/> | Obtiene o establece una matriz de datos adjuntos que se envían con el mensaje de correo electrónico.<br/>                      |
| [**Bcc**](emailaction-bcc.md)<br/>                   | Lectura y escritura<br/> | Obtiene o establece la dirección de correo electrónico o las direcciones que desea que se oculte en el mensaje de correo electrónico.<br/>         |
| [**Body**](emailaction-body.md)<br/>                 | Lectura y escritura<br/> | Obtiene o establece el cuerpo del correo electrónico que contiene el mensaje de correo electrónico.<br/>                            |
| [**Cc**](emailaction-cc.md)<br/>                     | Lectura y escritura<br/> | Obtiene o establece la dirección de correo electrónico o las direcciones que desea cc en el mensaje de correo electrónico.<br/>          |
| [**De**](emailaction-from.md)<br/>                 | Lectura y escritura<br/> | Obtiene o establece la dirección de correo electrónico desde la que desea enviar el correo electrónico.<br/>                           |
| [**HeaderFields**](emailaction-headerfields.md)<br/> | Lectura y escritura<br/> | Obtiene o establece la información de encabezado en el correo electrónico que desea enviar.<br/>                        |
| [**Id**](action-id.md)<br/>                          | Lectura y escritura<br/> | Se hereda del [**objeto Action.**](action.md) Obtiene o establece el identificador de la acción.<br/> |
| [**ReplyTo**](emailaction-replyto.md)<br/>           | Lectura y escritura<br/> | Obtiene o establece la dirección de correo electrónico a la que desea responder.<br/>                                      |
| [**Servidor**](emailaction-server.md)<br/>             | Lectura y escritura<br/> | Obtiene o establece el nombre del servidor desde el que se usa para enviar correo electrónico.<br/>                           |
| [**Asunto**](emailaction-subject.md)<br/>           | Lectura y escritura<br/> | Obtiene o establece el asunto del mensaje de correo electrónico.<br/>                                                 |
| [**En**](emailaction-to.md)<br/>                     | Lectura y escritura<br/> | Obtiene o establece la dirección de correo electrónico o las direcciones a las que desea enviar el correo electrónico.<br/>                |
| [**Tipo**](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | Solo lectura<br/>  | Se hereda del [**objeto Action.**](action.md) Obtiene el tipo de la acción.<br/>                   |



 

## <a name="remarks"></a>Observaciones

La acción de correo electrónico debe tener un valor válido para las propiedades [**Server**](emailaction-server.md), [**From**](emailaction-from.md)y [**To**](emailaction-to.md) o [**Cc**](emailaction-cc.md) para que la tarea se registre y se ejecute correctamente.

Al leer o escribir su propio XML para una tarea, se especifica una acción de correo electrónico mediante el [**elemento SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) del Programador de tareas esquema.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea [Ejemplo de desencadenador de eventos (scripting).](/previous-versions//aa446887(v=vs.85))

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                    |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

