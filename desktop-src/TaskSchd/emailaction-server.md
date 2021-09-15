---
title: EmailAction.Server, propiedad
description: Para el scripting, obtiene o establece el nombre del servidor SMTP desde el que se usa para enviar correo electrónico.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Propiedades de servidor Programador de tareas
- Propiedad de servidor Programador de tareas , objeto EmailAction
- Objeto EmailAction Programador de tareas propiedad , Server
topic_type:
- apiref
api_name:
- EmailAction.Server
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fefcc5e33727d6b4ad0bcd60e48432c68422105
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474666"
---
# <a name="emailactionserver-property"></a>EmailAction.Server, propiedad

\[Este objeto ya no se admite. Use IExecAction con el cmdlet [**Send-MailMessage de**](/powershell/module/microsoft.powershell.utility/send-mailmessage) PowerShell como solución alternativa.\]

Para el scripting, obtiene o establece el nombre del servidor SMTP desde el que se usa para enviar correo electrónico.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
EmailAction.Server As String
```



## <a name="property-value"></a>Valor de propiedad

Nombre del servidor desde el que se usa para enviar correo electrónico.

## <a name="remarks"></a>Observaciones

Asegúrese de que el servidor SMTP que envía el correo electrónico está configurado correctamente. El correo electrónico se envía mediante la autenticación NTLM para servidores SMTP de Windows, lo que significa que las credenciales de seguridad usadas para ejecutar la tarea también deben tener privilegios en el servidor SMTP para enviar un mensaje de correo electrónico. Si el servidor SMTP es un servidor no basado en Windows, se enviará el correo electrónico si el servidor permite el acceso anónimo. Para obtener información sobre cómo configurar el servidor [SMTP,](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)vea Programa de instalación del servidor SMTP y, para obtener información sobre cómo administrar la configuración del servidor SMTP, vea [Administración de SMTP.](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10))

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                    |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

