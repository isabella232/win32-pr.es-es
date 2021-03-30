---
title: Propiedad EmailAction. Attachments
description: En el caso de scripting, obtiene o establece una matriz de datos adjuntos que se envía con el mensaje de correo electrónico.
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- Programador de tareas de propiedades de datos adjuntos
- Propiedad Attachments Programador de tareas, objeto EmailAction
- Programador de tareas de objeto EmailAction, propiedad Attachments
topic_type:
- apiref
api_name:
- EmailAction.Attachments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae620321f9dca7a5c38decf7de661d713989c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802576"
---
# <a name="emailactionattachments-property"></a>Propiedad EmailAction. Attachments

\[Este objeto ya no se admite. Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.\]

En el caso de scripting, obtiene o establece una matriz de datos adjuntos que se envía con el mensaje de correo electrónico.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a>Valor de propiedad

Una matriz de datos adjuntos que se envía con el mensaje de correo electrónico.

## <a name="remarks"></a>Observaciones

Un máximo de ocho datos adjuntos puede estar en la matriz de datos adjuntos.

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

 

