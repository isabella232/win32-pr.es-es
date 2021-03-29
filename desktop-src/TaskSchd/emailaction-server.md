---
title: EmailAction. Server (propiedad)
description: En el caso de scripting, obtiene o establece el nombre del servidor SMTP que se usa para enviar correo electrónico desde.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Programador de tareas de propiedades de servidor
- Propiedad Server Programador de tareas, objeto EmailAction
- Programador de tareas de objeto EmailAction, propiedad de servidor
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359752"
---
# <a name="emailactionserver-property"></a>EmailAction. Server (propiedad)

\[Este objeto ya no se admite. Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.\]

En el caso de scripting, obtiene o establece el nombre del servidor SMTP que se usa para enviar correo electrónico desde.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
EmailAction.Server As String
```



## <a name="property-value"></a>Valor de propiedad

El nombre del servidor que se usa para enviar correo electrónico desde.

## <a name="remarks"></a>Observaciones

Asegúrese de que el servidor SMTP que envía el correo electrónico está configurado correctamente. El correo electrónico se envía mediante la autenticación NTLM para los servidores SMTP de Windows, lo que significa que las credenciales de seguridad utilizadas para ejecutar la tarea también deben tener privilegios en el servidor SMTP para enviar un mensaje de correo electrónico. Si el servidor SMTP no es un servidor basado en Windows, se enviará el correo electrónico si el servidor permite el acceso anónimo. Para obtener información acerca de la configuración del servidor SMTP, consulte [configuración](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)del servidor SMTP y, para obtener información acerca de la administración de la configuración del servidor SMTP, consulte [Administración de SMTP](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                    |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

