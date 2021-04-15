---
title: Elemento Command (execType)
description: Especifica el archivo ejecutable o el documento que se va a ejecutar.
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- Programador de tareas del elemento Command
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422522"
---
# <a name="command-exectype-element"></a>Elemento Command (execType)

Especifica el archivo ejecutable o el documento que se va a ejecutar.

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

El elemento **Command** se define mediante el tipo complejo [**execType**](taskschedulerschema-exectype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                      | Derivado de                                                 | Descripción                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Ejec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Especifica una acción que ejecuta una operación de línea de comandos.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea la [**propiedad arguments de IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).

Para el desarrollo de scripts, vea [**ExecAction. arguments**](execaction-arguments.md).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que usa una acción ejecutable, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





