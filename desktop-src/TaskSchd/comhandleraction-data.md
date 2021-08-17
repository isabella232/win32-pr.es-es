---
title: ComHandlerAction.Data, propiedad
description: Para el scripting, obtiene o establece datos adicionales asociados al controlador.
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- Propiedades de datos Programador de tareas
- Propiedad data Programador de tareas , objeto ComHandlerAction
- Objeto ComHandlerAction Programador de tareas , propiedad Data
topic_type:
- apiref
api_name:
- ComHandlerAction.Data
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254457941d55d9a6b130ec504563236e60baf7ba1a1d44d5851ed3c712634afb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139608"
---
# <a name="comhandleractiondata-property"></a>ComHandlerAction.Data, propiedad

Para el scripting, obtiene o establece datos adicionales asociados al controlador.

## <a name="syntax"></a>Syntax


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a>Valor de propiedad

Argumentos necesarios para el controlador.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML, los datos de un controlador COM se especifican en el [**elemento Data**](taskschedulerschema-data-comhandlertype-element.md) del Programador de tareas esquema.

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

 

 





