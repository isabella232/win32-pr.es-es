---
title: Objeto TaskVariables
description: Objeto de scripting que define variables de tarea que se pueden pasar como parámetros a controladores de tareas y ejecutables externos que inician las tareas.
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- Objetos TaskVariables Programador de tareas
- Objeto TaskVariables Programador de tareas , descrito
topic_type:
- apiref
api_name:
- TaskVariables
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ada89af03a735dca3957144e08857b03ca6824609b3c1ce6e50a46ce95d7fa0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575055"
---
# <a name="taskvariables-object"></a>Objeto TaskVariables

Objeto de scripting que define variables de tarea que se pueden pasar como parámetros a controladores de tareas y ejecutables externos que inician las tareas.

## <a name="members"></a>Miembros

El **objeto TaskVariables** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto TaskVariables** tiene estos métodos.



| Método                                         | Descripción                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**GetContext**](taskvariables-getcontext.md) | Se usa para compartir el contexto entre diferentes pasos y tareas que se encuentran en la misma instancia de trabajo.<br/> |
| [**GetInput**](taskvariables-getinput.md)     | Obtiene las variables de entrada de una tarea.<br/>                                                           |
| [**SetOutput**](taskvariables-setoutput.md)   | Establece las variables de salida de una tarea.<br/>                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





