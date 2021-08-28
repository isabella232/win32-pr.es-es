---
title: Elemento Exec (actionGroup)
description: Especifica una acción que ejecuta una operación de línea de comandos.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Exec, elemento Programador de tareas
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 709cded1238654fffcf8ce75e5cba85c6139eb6264592e99684462e0a9cb2661
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072495"
---
# <a name="exec-actiongroup-element"></a>Elemento Exec (actionGroup)

Especifica una acción que ejecuta una operación de línea de comandos.

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

El **elemento Exec** se define mediante [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                         | Derivado de                                                       | Descripción                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Acciones**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contiene las acciones realizadas por la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                           | Tipo       | Descripción                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [**Argumentos**](taskschedulerschema-arguments-exectype-element.md)               | **string** | Especifica los argumentos asociados a la operación de línea de comandos.<br/>                               |
| [**Comando**](taskschedulerschema-command-exectype-element.md)                   | **string** | Especifica el archivo ejecutable o el documento que se va a ejecutar.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | string     | Especifica el directorio donde existe el archivo ejecutable o los archivos utilizados por el ejecutable.<br/> |



## <a name="attributes"></a>Atributos



| Nombre | Tipo       | Descripción                                                    |
|------|------------|----------------------------------------------------------------|
| id   | **string** | Identificador de la acción realizada por la tarea.<br/> |



## <a name="remarks"></a>Comentarios

El tipo complejo [**execType**](taskschedulerschema-exectype-complextype.md) define los elementos secundarios enumerados anteriormente.

Para el desarrollo de scripts, el objeto [**ExecAction**](execaction.md) define una acción de ejecución.

Para el desarrollo de C++, la interfaz [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) define una acción de ejecución.

Si se usan variables de entorno en los elementos [**Command**](taskschedulerschema-command-exectype-element.md), [**Arguments**](taskschedulerschema-arguments-exectype-element.md)o [**WorkingDirectory,**](taskschedulerschema-workingdirectory-exectype-element.md) los valores de las variables de entorno se almacenan en caché y se usan cuando se inicia el Taskeng.exe (el motor de tareas). El motor de tareas no usará los cambios en las variables de entorno que se producen después de iniciar el motor de tareas.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML para una tarea que usa un desencadenador de eventos, vea Ejemplo de desencadenador [de tiempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





