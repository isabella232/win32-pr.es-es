---
title: Objeto TaskNamedValuePair
description: Objeto de scripting que se usa para crear un par nombre-valor en el que el nombre está asociado al valor.
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- Objeto TaskNamedValuePair Programador de tareas
- Programador de tareas de objeto TaskNamedValuePair, descrito
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
ms.openlocfilehash: b95229b5714d2cdcc43a071f2e51a50e04706429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685886"
---
# <a name="tasknamedvaluepair-object"></a>Objeto TaskNamedValuePair

Objeto de scripting que se usa para crear un par nombre-valor en el que el nombre está asociado al valor.

## <a name="members"></a>Miembros

El objeto **TaskNamedValuePair** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **TaskNamedValuePair** tiene estas propiedades.



| Propiedad                                             | Descripción                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**Name**](tasknamedvaluepair-name.md)<br/>   | Obtiene o establece el nombre asociado a un valor en un par nombre-valor.<br/> |
| [**Value**](tasknamedvaluepair-value.md)<br/> | Obtiene o establece el valor asociado a un nombre en un par nombre-valor.<br/> |



 

## <a name="remarks"></a>Observaciones

Al leer o escribir su propio XML para una tarea, se especifica un par de nombre y valor mediante el elemento [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TaskNamedValueCollection**](tasknamedvaluecollection.md)
</dt> </dl>

 

 





