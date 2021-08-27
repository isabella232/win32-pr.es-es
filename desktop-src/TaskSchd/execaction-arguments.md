---
title: Propiedad ExecAction.Arguments
description: Para el scripting, obtiene o establece los argumentos asociados a la operación de línea de comandos.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Propiedades arguments Programador de tareas
- Propiedad Arguments Programador de tareas , objeto ExecAction
- Objeto ExecAction Programador de tareas propiedad , Arguments
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899e4ceaaf3a0d04dc678592add18184401d54569fea71f0570a0acbf2a33027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011495"
---
# <a name="execactionarguments-property"></a>Propiedad ExecAction.Arguments

Para el scripting, obtiene o establece los argumentos asociados a la operación de línea de comandos.

## <a name="syntax"></a>Syntax


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a>Valor de propiedad

Argumentos necesarios para la operación de línea de comandos.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML, los argumentos de la operación de línea de comandos se especifican en el [**elemento Arguments**](taskschedulerschema-arguments-exectype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





