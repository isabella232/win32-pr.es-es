---
title: Propiedad ComHandlerAction. ClassId
description: Para scripting, obtiene o establece el identificador de la clase de controlador.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- Propiedad ClassId Programador de tareas
- Propiedad ClassId Programador de tareas, objeto ComHandlerAction
- Programador de tareas objeto ComHandlerAction, propiedad ClassId
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
ms.openlocfilehash: 30409d5ea8067d1148bf42c88e2a3d1bb6f65ad1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801801"
---
# <a name="comhandleractionclassid-property"></a>Propiedad ComHandlerAction. ClassId

Para scripting, obtiene o establece el identificador de la clase de controlador.

## <a name="syntax"></a>Sintaxis


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a>Valor de propiedad

Identificador de la clase que define el controlador que se va a desencadenar.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML, la clase de un controlador COM se especifica en el elemento [**ClassID**](taskschedulerschema-classid-comhandlertype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





