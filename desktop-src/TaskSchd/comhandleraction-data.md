---
title: Propiedad ComHandlerAction. Data
description: Para scripting, obtiene o establece datos adicionales asociados al controlador.
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- Programador de tareas de propiedades de datos
- Programador de tareas de propiedad de datos, objeto ComHandlerAction
- Programador de tareas de objeto ComHandlerAction, propiedad de datos
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
ms.openlocfilehash: 15743c3f787a591a4644081fdd63189829d2eab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422549"
---
# <a name="comhandleractiondata-property"></a>Propiedad ComHandlerAction. Data

Para scripting, obtiene o establece datos adicionales asociados al controlador.

## <a name="syntax"></a>Sintaxis


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a>Valor de propiedad

Argumentos necesarios para el controlador.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML, los datos de un controlador COM se especifican en el elemento de [**datos**](taskschedulerschema-data-comhandlertype-element.md) del esquema de programador de tareas.

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

 

 





