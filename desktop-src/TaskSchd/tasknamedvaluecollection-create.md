---
title: Método TaskNamedValueCollection.Create
description: Para el scripting, crea un par nombre-valor en la colección.
ms.assetid: f64e0548-fad3-4682-b50b-ff8ec685af36
keywords:
- Creación de métodos Programador de tareas
- Create method Programador de tareas , TaskNamedValueCollection object
- TaskNamedValueCollection object Programador de tareas , Create (método)
topic_type:
- apiref
api_name:
- TaskNamedValueCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d974eb7fb93d3bb617ce122426b4003a708cbe3ed753ba758fdd5f71ed8bc87a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118858074"
---
# <a name="tasknamedvaluecollectioncreate-method"></a>Método TaskNamedValueCollection.Create

Para el scripting, crea un par nombre-valor en la colección.

## <a name="syntax"></a>Sintaxis


```VB
TaskNamedValueCollection.Create( _
  ByVal name, _
  ByVal value, _
  ByRef pair _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* \[ En\]
</dt> <dd>

Nombre asociado a un valor en un par nombre-valor.

</dd> <dt>

*value* \[ En\]
</dt> <dd>

Valor asociado a un nombre en un par nombre-valor.

</dd> <dt>

*pair* \[ out\]
</dt> <dd>

Par nombre-valor que se crea en la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





