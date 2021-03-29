---
title: Objeto ActionCollection
description: Objeto de scripting que contiene las acciones realizadas por la tarea.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- Actions Programador de tareas, Collection (objeto)
- Objeto ActionCollection Programador de tareas
- Programador de tareas de objeto ActionCollection, descrito
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dee7182cc79684dec1fd052f7ad67409ba513f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535506"
---
# <a name="actioncollection-object"></a>Objeto ActionCollection

Objeto de scripting que contiene las acciones realizadas por la tarea.

## <a name="members"></a>Miembros

El objeto **ActionCollection** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **ActionCollection** tiene estos métodos.



| Método                                    | Descripción                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [**Claridad**](actioncollection-clear.md)   | Borra todas las acciones de la colección.<br/>      |
| [**A**](actioncollection-create.md) | Crea y agrega una nueva acción a la colección.<br/> |
| [**Retirar**](actioncollection-remove.md) | Quita una acción especificada de la colección.<br/>  |



 

### <a name="properties"></a>Propiedades

El objeto **ActionCollection** tiene estas propiedades.



| Propiedad                                               | Tipo de acceso           | Descripción                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Context**](actioncollection-context.md)<br/> | Lectura/escritura<br/> | Obtiene o establece el identificador de la entidad de seguridad para la tarea.<br/> |
| [**Contabiliza**](actioncollection-count.md)<br/>     | Solo lectura<br/>  | Obtiene el número de acciones de la colección.<br/>              |
| [**Elemento**](actioncollection-item.md)<br/>       | Solo lectura<br/>  | Obtiene una acción especificada de la colección.<br/>               |
| [**XmlText**](actioncollection-xmltext.md)<br/> | Lectura/escritura<br/> | Obtiene o establece una versión con formato XML de la colección.<br/>   |



 

## <a name="remarks"></a>Observaciones

Al leer o escribir XML, las acciones de una tarea se especifican en el elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) del esquema programador de tareas.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md), ejemplo de desencadenador de [eventos (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))scripting), ejemplo de [desencadenador diario (](daily-trigger-example--scripting-.md)scripting), ejemplo [de](boot-trigger-example--scripting-.md) [desencadenador de registro (](registration-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador semanal (](weekly-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador de inicio de sesión](logon-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





