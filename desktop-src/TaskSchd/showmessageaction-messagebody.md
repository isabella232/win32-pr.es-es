---
title: Propiedad ShowMessageAction. MessageBody
description: En el caso de scripting, obtiene o establece el texto del mensaje que se muestra en el cuerpo del cuadro de mensaje.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- Programador de tareas de la propiedad MessageBody
- Programador de tareas de la propiedad MessageBody, objeto ShowMessageAction
- Programador de tareas de objeto ShowMessageAction, propiedad MessageBody
topic_type:
- apiref
api_name:
- ShowMessageAction.MessageBody
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1604367a8daad1ae1b5f44c6021d22bf1aa7c5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905088"
---
# <a name="showmessageactionmessagebody-property"></a>Propiedad ShowMessageAction. MessageBody

\[Este objeto ya no se admite. Puede usar IExecAction con la [**función MsgBox**](/previous-versions/sfw6660x(v=vs.80)) de scripting de Windows para mostrar un mensaje en la sesión de usuario.\]

En el caso de scripting, obtiene o establece el texto del mensaje que se muestra en el cuerpo del cuadro de mensaje.

## <a name="syntax"></a>Sintaxis


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a>Valor de propiedad

Texto del mensaje que se muestra en el cuerpo del cuadro de mensaje.

## <a name="remarks"></a>Observaciones

Las cadenas con parámetros se pueden usar en el texto del mensaje del cuadro de mensaje. Para obtener más información, vea la sección ejemplos en [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).

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

[**ShowMessageAction**](showmessageaction.md)
</dt> </dl>

 

