---
title: Principal.Id propiedad
description: Para el scripting, obtiene o establece el identificador de la entidad de seguridad.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- Identificador de propiedad Programador de tareas
- Id, propiedad Programador de tareas , objeto Principal
- Objeto principal Programador de tareas , propiedad Id
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173033"
---
# <a name="principalid-property"></a>Principal.Id propiedad

Para el scripting, obtiene o establece el identificador de la entidad de seguridad.

## <a name="syntax"></a>Sintaxis


```VB
Principal.Id As String
```



## <a name="property-value"></a>Valor de propiedad

El identificador de la entidad de seguridad.

## <a name="remarks"></a>Observaciones

Este identificador también se usa al especificar la [**propiedad ActionCollection.Context.**](actioncollection-context.md)

Al leer o escribir XML para una tarea, el identificador de la entidad de seguridad se especifica en el atributo Id del elemento [**Principal**](taskschedulerschema-principal-principaltype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ActionCollection.Context**](actioncollection-context.md)
</dt> <dt>

[**Principal**](principal.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





