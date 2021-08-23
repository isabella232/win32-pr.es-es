---
title: Objeto TriggerCollection (Windows.ui.xaml.h)
description: Objeto de scripting que se usa para agregar, quitar y recuperar los desencadenadores de una tarea.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- desencadenadores Programador de tareas , desencadenar objeto de colección
- Desencadenador de objetos TriggerCollection Programador de tareas
- Objeto TriggerCollection Programador de tareas , descrito
topic_type:
- apiref
api_name:
- TriggerCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fd103918bc3898e56a3041221c9c70c9ede9aea5df4843cd984f2502279014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001943"
---
# <a name="triggercollection-object"></a>Objeto TriggerCollection

Objeto de scripting que se usa para agregar, quitar y recuperar los desencadenadores de una tarea.

## <a name="members"></a>Miembros

El **objeto TriggerCollection** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto TriggerCollection** tiene estos métodos.



| Método                                     | Descripción                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Borrar**](triggercollection-clear.md)   | Borra todos los desencadenadores de la colección.<br/>                                        |
| [**Crear**](triggercollection-create.md) | Crea un nuevo desencadenador para la tarea.<br/>                                             |
| [**Quitar**](triggercollection-remove.md) | Quita el desencadenador especificado de la colección de desencadenadores usados por la tarea.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto TriggerCollection** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso          | Descripción                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Count**](triggercollection-count.md)<br/> | Solo lectura<br/> | Obtiene el número de desencadenadores de la colección.<br/>  |
| [**Elemento**](triggercollection-item.md)<br/>   | Solo lectura<br/> | Obtiene el desencadenador especificado de la colección.<br/> |



 

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, los desencadenadores de la tarea se especifican en el elemento [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) del Programador de tareas esquema.

Para obtener información sobre cada tipo de desencadenador, vea [Tipos de desencadenador.](trigger-types.md)

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea [Ejemplo de desencadenador de tiempo (scripting).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Windows.ui.xaml.h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl>      |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**detonante**](trigger.md)
</dt> </dl>

 

 





