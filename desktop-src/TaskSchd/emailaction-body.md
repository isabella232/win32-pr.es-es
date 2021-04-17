---
title: EmailAction. Body (propiedad)
description: En el caso de scripting, obtiene o establece el cuerpo del correo electrónico que contiene el mensaje de correo electrónico.
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- Propiedad del cuerpo Programador de tareas
- Propiedad Body Programador de tareas, objeto EmailAction
- Programador de tareas de objeto EmailAction, propiedad Body
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
ms.openlocfilehash: 84be176fcf63c7a5191588dc0a68ccaf06c69f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676781"
---
# <a name="emailactionbody-property"></a>EmailAction. Body (propiedad)

\[Este objeto ya no se admite. Use IExecAction con el cmdlet [**send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) de PowerShell como solución alternativa.\]

En el caso de scripting, obtiene o establece el cuerpo del correo electrónico que contiene el mensaje de correo electrónico.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
EmailAction.Body As String
```



## <a name="property-value"></a>Valor de propiedad

El cuerpo del correo electrónico que contiene el mensaje de correo electrónico.

## <a name="remarks"></a>Observaciones

Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un archivo resource. dll. Una cadena especializada se usa para hacer referencia al texto del archivo de recursos. El formato de la cadena es $ (@ \[ dll \] , \[ resourceId \] ), donde \[ dll \] es la ruta de acceso al archivo. dll que contiene el recurso y \[ resourceId \] es el identificador del texto del recurso. Por ejemplo, al establecer este valor de propiedad en $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101), la propiedad se establecerá en el valor del texto del recurso con un identificador igual a-101 en el archivo% SystemRoot% \\ system32 \\ResourceName.dll.

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

 

