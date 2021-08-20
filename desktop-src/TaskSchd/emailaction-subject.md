---
title: Propiedad EmailAction.Subject
description: Para el scripting, obtiene o establece el asunto del mensaje de correo electrónico.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Propiedad subject Programador de tareas
- Propiedad Subject Programador de tareas , objeto EmailAction
- Objeto EmailAction Programador de tareas , propiedad Subject
topic_type:
- apiref
api_name:
- EmailAction.Subject
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7474fa4b7a6de59fd59a98c27a4877ab10c1acb6beac3c1682fccd05702aa275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943792"
---
# <a name="emailactionsubject-property"></a>Propiedad EmailAction.Subject

\[Este objeto ya no se admite. Use IExecAction con el cmdlet [**Send-MailMessage de**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) PowerShell como solución alternativa.\]

Para el scripting, obtiene o establece el asunto del mensaje de correo electrónico.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a>Valor de propiedad

Asunto del mensaje de correo electrónico.

## <a name="remarks"></a>Comentarios

Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un recurso .dll archivo. Se usa una cadena especializada para hacer referencia al texto del archivo de recursos. El formato de la cadena es $(@ Dll , ResourceID ), donde Dll es la ruta de acceso al archivo .dll que contiene el recurso y ResourceID es el identificador del texto \[ \] del \[ \] \[ \] \[ \] recurso. Por ejemplo, el establecimiento de este valor de propiedad en $(@ %SystemRoot% \\ System32ResourceName.dll, -101) establecerá la propiedad en el valor del texto del recurso con un identificador igual a -101 en el archivo deResourceName.dll \\ %SystemRoot%. \\ \\

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

