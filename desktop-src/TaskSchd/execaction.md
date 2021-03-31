---
title: Objeto ExecAction
description: Objeto de scripting que representa una acción que ejecuta una operación de línea de comandos.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- ejecutar acción Programador de tareas, interfaz
- Objeto ExecAction Programador de tareas
- Programador de tareas de objeto ExecAction, descrito
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cddd1b9b44612b4ce896fb3ceb99a6deeaa5e3a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150956"
---
# <a name="execaction-object"></a>Objeto ExecAction

Objeto de scripting que representa una acción que ejecuta una operación de línea de comandos.

## <a name="members"></a>Miembros

El objeto **ExecAction** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **ExecAction** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**Argumentos**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | Lectura/escritura<br/> | Obtiene o establece los argumentos asociados a la operación de la línea de comandos.<br/>                                                 |
| [**Sesión**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | Lectura/escritura<br/> | Heredado del objeto de [**acción**](action.md) . Obtiene o establece el identificador de la acción.<br/>                         |
| [**Ruta**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | Lectura/escritura<br/> | Obtiene o establece la ruta de acceso a un archivo ejecutable.<br/>                                                                           |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | Solo lectura<br/>  | Heredado del objeto de [**acción**](action.md) . Obtiene el tipo de la acción.<br/>                                       |
| [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | Lectura/escritura<br/> | Obtiene o establece el directorio que contiene el archivo ejecutable o los archivos utilizados por el archivo ejecutable.<br/> |



 

## <a name="remarks"></a>Observaciones

Si se usan variables de entorno en las propiedades [**path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)o [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) , los valores de las variables de entorno se almacenan en caché y se usan cuando se inicia el Taskeng.exe (el motor de tareas). El motor de tareas no utilizará los cambios en las variables de entorno que se producen después de iniciar el motor de tareas.

Esta acción realiza una operación de línea de comandos. Por ejemplo, la acción podría ejecutar un script o iniciar un ejecutable.

Al leer o escribir XML, se especifica una acción de ejecución en el elemento [**exec**](taskschedulerschema-exec-actiongroup-element.md) del esquema de programador de tareas.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





