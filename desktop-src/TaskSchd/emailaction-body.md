---
title: Propiedad EmailAction.Body
description: Para el scripting, obtiene o establece el cuerpo del correo electrónico que contiene el mensaje de correo electrónico.
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- Propiedades body Programador de tareas
- Propiedad body Programador de tareas , objeto EmailAction
- Objeto EmailAction Programador de tareas , propiedad Body
topic_type:
- apiref
api_name:
- EmailAction.Body
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57daf8d16da9f77a88d91a23cfaea88d1c3e27adb09a0d502b447b5987fce2ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100385"
---
# <a name="emailactionbody-property"></a>Propiedad EmailAction.Body

\[Este objeto ya no se admite. Use IExecAction con el cmdlet [**Send-MailMessage de**](/powershell/module/microsoft.powershell.utility/send-mailmessage) PowerShell como solución alternativa.\]

Para el scripting, obtiene o establece el cuerpo del correo electrónico que contiene el mensaje de correo electrónico.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Body As String
```



## <a name="property-value"></a>Valor de propiedad

Cuerpo del correo electrónico que contiene el mensaje de correo electrónico.

## <a name="remarks"></a>Comentarios

Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un recurso .dll archivo. Se usa una cadena especializada para hacer referencia al texto del archivo de recursos. El formato de la cadena es $(@ Dll , ResourceID ), donde Dll es la ruta de acceso al archivo .dll que contiene el recurso y ResourceID es el identificador del texto \[ \] del \[ \] \[ \] \[ \] recurso. Por ejemplo, el establecimiento de este valor de propiedad en $(@ %SystemRoot% \\ System32ResourceName.dll, -101) establecerá la propiedad en el valor del texto del recurso con un identificador igual a -101 en el archivo deResourceName.dll \\ %SystemRoot%. \\ \\

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

 

