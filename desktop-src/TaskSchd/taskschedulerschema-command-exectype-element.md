---
title: Elemento Command (execType)
description: Especifica el archivo ejecutable o el documento que se va a ejecutar.
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- Elemento Command Programador de tareas
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9d27eb5b40d652035882efc311d9735bcbdd23e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071048"
---
# <a name="command-exectype-element"></a>Elemento Command (execType)

Especifica el archivo ejecutable o el documento que se va a ejecutar.

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

El tipo complejo [**execType**](taskschedulerschema-exectype-complextype.md) define el elemento **Command.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                      | Derivado de                                                 | Descripción                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Especifica una acción que ejecuta una operación de línea de comandos.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea la [**propiedad Arguments de IExecAction.**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)

Para el desarrollo de scripts, [**vea ExecAction.Arguments**](execaction-arguments.md).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que usa una acción ejecutable, vea Ejemplo de desencadenador de tiempo [(XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





