---
title: Propiedad EmailAction.Attachments
description: Para el scripting, obtiene o establece una matriz de datos adjuntos que se envían con el mensaje de correo electrónico.
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- Propiedad Attachments Programador de tareas
- Propiedad Attachments Programador de tareas , objeto EmailAction
- Objeto EmailAction Programador de tareas , propiedad Attachments
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
ms.openlocfilehash: cbd43622c7755df2eb8bc2f02416396f55e59dcb5f82ffe6434a84e05a9358ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100425"
---
# <a name="emailactionattachments-property"></a>Propiedad EmailAction.Attachments

\[Este objeto ya no se admite. Use IExecAction con el cmdlet [**Send-MailMessage de**](/powershell/module/microsoft.powershell.utility/send-mailmessage) PowerShell como solución alternativa.\]

Para el scripting, obtiene o establece una matriz de datos adjuntos que se envían con el mensaje de correo electrónico.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a>Valor de propiedad

Matriz de datos adjuntos que se envía con el mensaje de correo electrónico.

## <a name="remarks"></a>Comentarios

Un máximo de ocho datos adjuntos pueden estar en la matriz de datos adjuntos.

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

 

