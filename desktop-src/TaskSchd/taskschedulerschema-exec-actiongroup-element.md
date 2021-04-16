---
title: Exec (actionGroup), elemento
description: Especifica una acción que ejecuta una operación de línea de comandos.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Elemento exec Programador de tareas
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105678651"
---
# <a name="exec-actiongroup-element"></a>Exec (actionGroup), elemento

Especifica una acción que ejecuta una operación de línea de comandos.

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

El elemento **exec** está definido por [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                         | Derivado de                                                       | Descripción                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Acciones**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contiene las acciones realizadas por la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                           | Tipo       | Descripción                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [**Argumentos**](taskschedulerschema-arguments-exectype-element.md)               | **string** | Especifica los argumentos asociados con la operación de línea de comandos.<br/>                               |
| [**Get-Help**](taskschedulerschema-command-exectype-element.md)                   | **string** | Especifica el archivo ejecutable o el documento que se va a ejecutar.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | string     | Especifica el directorio donde existe el archivo ejecutable o los archivos utilizados por el archivo ejecutable.<br/> |



## <a name="attributes"></a>Atributos



| Nombre | Tipo       | Descripción                                                    |
|------|------------|----------------------------------------------------------------|
| id   | **string** | Identificador de la acción realizada por la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Los elementos secundarios enumerados anteriormente se definen mediante el tipo complejo [**execType**](taskschedulerschema-exectype-complextype.md) .

Para el desarrollo de scripts, se define una acción de ejecución mediante el objeto [**ExecAction**](execaction.md) .

En el desarrollo de C++, la interfaz [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) define una acción de ejecución.

Si se usan variables de entorno en los elementos [**Command**](taskschedulerschema-command-exectype-element.md), [**arguments**](taskschedulerschema-arguments-exectype-element.md)o [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) , los valores de las variables de entorno se almacenan en caché y se usan cuando se inicia el Taskeng.exe (el motor de tareas). El motor de tareas no utilizará los cambios en las variables de entorno que se producen después de iniciar el motor de tareas.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que utiliza un desencadenador de eventos, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





