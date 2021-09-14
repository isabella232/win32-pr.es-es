---
title: Propiedad ShowMessageAction.MessageBody
description: Para el scripting, obtiene o establece el texto del mensaje que se muestra en el cuerpo del cuadro de mensaje.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- Propiedad MessageBody Programador de tareas
- Propiedad MessageBody Programador de tareas , objeto ShowMessageAction
- Objeto ShowMessageAction Programador de tareas , propiedad MessageBody
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886505"
---
# <a name="showmessageactionmessagebody-property"></a>Propiedad ShowMessageAction.MessageBody

\[Este objeto ya no se admite. Puede usar IExecAction con la función [**msgbox**](/previous-versions/sfw6660x(v=vs.80)) Windows scripting para mostrar un mensaje en la sesión de usuario.\]

Para el scripting, obtiene o establece el texto del mensaje que se muestra en el cuerpo del cuadro de mensaje.

## <a name="syntax"></a>Sintaxis


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a>Valor de propiedad

Texto del mensaje que se muestra en el cuerpo del cuadro de mensaje.

## <a name="remarks"></a>Observaciones

Las cadenas parametrizadas se pueden usar en el texto del mensaje del cuadro de mensaje. Para obtener más información, vea la sección Ejemplos [**de EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).

Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un recurso .dll archivo. Se usa una cadena especializada para hacer referencia al texto del archivo de recursos. El formato de la cadena es $(@ Dll , ResourceID ), donde Dll es la ruta de acceso al archivo .dll que contiene el recurso y ResourceID es el identificador del texto \[ \] del \[ \] \[ \] \[ \] recurso. Por ejemplo, el establecimiento de este valor de propiedad en $(@ %SystemRoot% System32ResourceName.dll, -101) establecerá la propiedad en el valor del texto del recurso con un identificador igual a -101 en el archivo deResourceName.dll \\ \\ %SystemRoot% \\ \\ System32.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                    |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ShowMessageAction**](showmessageaction.md)
</dt> </dl>

 

