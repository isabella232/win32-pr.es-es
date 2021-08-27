---
title: ComHandlerAction.ClassId, propiedad
description: Para el scripting, obtiene o establece el identificador de la clase de controlador.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- Propiedad ClassId Programador de tareas
- Propiedad ClassId Programador de tareas , objeto ComHandlerAction
- Objeto ComHandlerAction Programador de tareas , propiedad ClassId
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72338d4fe15936fcfe8f158098a798c4a3630cbd0587f46dc2f9346405477a59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100465"
---
# <a name="comhandleractionclassid-property"></a>ComHandlerAction.ClassId, propiedad

Para el scripting, obtiene o establece el identificador de la clase de controlador.

## <a name="syntax"></a>Syntax


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a>Valor de propiedad

Identificador de la clase que define el controlador que se va a desencadenar.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML, la clase de un controlador COM se especifica en el [**elemento ClassId**](taskschedulerschema-classid-comhandlertype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





