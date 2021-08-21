---
title: Objeto TaskNamedValuePair
description: Objeto de scripting que se usa para crear un par nombre-valor en el que el nombre está asociado al valor.
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- TaskNamedValuePair object Programador de tareas
- Objeto TaskNamedValuePair Programador de tareas , descrito
topic_type:
- apiref
api_name:
- TaskNamedValuePair
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fe41e839e5866d5a8c906a226c8db17c6ecae642d51d55d123d05a9b078a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118858041"
---
# <a name="tasknamedvaluepair-object"></a>Objeto TaskNamedValuePair

Objeto de scripting que se usa para crear un par nombre-valor en el que el nombre está asociado al valor.

## <a name="members"></a>Miembros

El **objeto TaskNamedValuePair** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto TaskNamedValuePair** tiene estas propiedades.



| Propiedad                                             | Descripción                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**Nombre**](tasknamedvaluepair-name.md)<br/>   | Obtiene o establece el nombre asociado a un valor en un par nombre-valor.<br/> |
| [**Valor**](tasknamedvaluepair-value.md)<br/> | Obtiene o establece el valor asociado a un nombre en un par nombre-valor.<br/> |



 

## <a name="remarks"></a>Comentarios

Al leer o escribir su propio XML para una tarea, se especifica un par nombre-valor mediante el elemento [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) del esquema Programador de tareas datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TaskNamedValueCollection**](tasknamedvaluecollection.md)
</dt> </dl>

 

 





