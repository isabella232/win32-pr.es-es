---
title: Elemento Arguments (execType)
description: Especifica los argumentos asociados a la operación de línea de comandos.
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Elemento Arguments Programador de tareas
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edf76f7073e62aac10c85dc035d3b441a90a4e0ee1fae90b4decf5cffc4568df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132080"
---
# <a name="arguments-exectype-element"></a>Elemento Arguments (execType)

Especifica los argumentos asociados a la operación de línea de comandos.

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

El **elemento Arguments** se define mediante el [**tipo complejo execType.**](taskschedulerschema-exectype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                      | Derivado de                                                 | Descripción                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Especifica una acción que ejecuta una operación de línea de comandos.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, vea la [**propiedad Arguments de IExecAction.**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)

Para el desarrollo de scripts, [**vea ExecAction.Arguments**](execaction-arguments.md).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que usa una acción ejecutable, vea Ejemplo de desencadenador de tiempo [(XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





