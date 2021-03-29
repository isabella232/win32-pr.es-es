---
title: Objeto TaskVariables
description: Objeto de scripting que define las variables de tarea que se pueden pasar como parámetros a los controladores de tareas y los archivos ejecutables externos iniciados por las tareas.
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- Objeto TaskVariables Programador de tareas
- Programador de tareas de objeto TaskVariables, descrito
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
ms.openlocfilehash: 00fe20153b0d6d66ca6c7f263a8e76d5a4d480b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492244"
---
# <a name="taskvariables-object"></a>Objeto TaskVariables

Objeto de scripting que define las variables de tarea que se pueden pasar como parámetros a los controladores de tareas y los archivos ejecutables externos iniciados por las tareas.

## <a name="members"></a>Miembros

El objeto **TaskVariables** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El objeto **TaskVariables** tiene estos métodos.



| Método                                         | Descripción                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**GetContext**](taskvariables-getcontext.md) | Se usa para compartir el contexto entre diferentes pasos y tareas que se encuentran en la misma instancia de trabajo.<br/> |
| [**GetInput**](taskvariables-getinput.md)     | Obtiene las variables de entrada para una tarea.<br/>                                                           |
| [**SetOutput**](taskvariables-setoutput.md)   | Establece las variables de salida de una tarea.<br/>                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





