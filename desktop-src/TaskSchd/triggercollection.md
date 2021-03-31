---
title: Objeto TriggerCollection (Windows. UI. Xaml. h)
description: Objeto de scripting que se utiliza para agregar, quitar y recuperar los desencadenadores de una tarea.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- desencadenadores Programador de tareas, objeto de colección de desencadenador
- Objeto TriggerCollection Programador de tareas
- Programador de tareas de objeto TriggerCollection, descrito
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
ms.openlocfilehash: 29f7288d8db0b56fc9cc8b3de7ace8c10c13959a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150090"
---
# <a name="triggercollection-object"></a>Objeto TriggerCollection

Objeto de scripting que se utiliza para agregar, quitar y recuperar los desencadenadores de una tarea.

## <a name="members"></a>Miembros

El objeto **TriggerCollection** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **TriggerCollection** tiene estos métodos.



| Método                                     | Descripción                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Claridad**](triggercollection-clear.md)   | Borra todos los desencadenadores de la colección.<br/>                                        |
| [**A**](triggercollection-create.md) | Crea un nuevo desencadenador para la tarea.<br/>                                             |
| [**Retirar**](triggercollection-remove.md) | Quita el desencadenador especificado de la colección de desencadenadores utilizada por la tarea.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **TriggerCollection** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso          | Descripción                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Contabiliza**](triggercollection-count.md)<br/> | Solo lectura<br/> | Obtiene el número de desencadenadores de la colección.<br/>  |
| [**Elemento**](triggercollection-item.md)<br/>   | Solo lectura<br/> | Obtiene el desencadenador especificado de la colección.<br/> |



 

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, los desencadenadores de la tarea se especifican en el elemento [**triggers**](taskschedulerschema-triggers-tasktype-element.md) del esquema de programador de tareas.

Para obtener información acerca de cada tipo de desencadenador, consulte [tipos de desencadenador](trigger-types.md).

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Windows. UI. Xaml. h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl>      |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Activado**](trigger.md)
</dt> </dl>

 

 





