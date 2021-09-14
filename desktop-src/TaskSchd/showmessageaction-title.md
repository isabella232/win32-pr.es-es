---
title: Propiedad ShowMessageAction.Title
description: Para el scripting, obtiene o establece el título del cuadro de mensaje.
ms.assetid: f61177fc-287c-4da9-9bdc-88aaa6868204
keywords:
- Propiedad Title Programador de tareas
- Propiedad Title Programador de tareas , objeto ShowMessageAction
- Objeto ShowMessageAction Programador de tareas , propiedad Title
topic_type:
- apiref
api_name:
- ShowMessageAction.Title
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e552bb51653248e0a70ccfc0edea907749900e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886508"
---
# <a name="showmessageactiontitle-property"></a>Propiedad ShowMessageAction.Title

\[Este objeto ya no se admite. Puede usar IExecAction con la función Windows scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) para mostrar un mensaje en la sesión de usuario.\]

Para el scripting, obtiene o establece el título del cuadro de mensaje.

## <a name="syntax"></a>Sintaxis


```VB
ShowMessageAction.Title As String
```



## <a name="property-value"></a>Valor de propiedad

Título del cuadro de mensaje.

## <a name="remarks"></a>Observaciones

Las cadenas parametrizadas se pueden usar en el texto del título del cuadro de mensaje. Para obtener más información, vea la sección Ejemplos de [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).

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

 

