---
title: Objeto ExecAction
description: Objeto de scripting que representa una acción que ejecuta una operación de línea de comandos.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- ejecutar acción Programador de tareas , interfaz
- ExecAction object Programador de tareas
- Objeto ExecAction Programador de tareas , descrito
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
ms.openlocfilehash: 140ff991bd26f779beee7407666572d8649bd9f1a2718b719713770745157656
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072665"
---
# <a name="execaction-object"></a>Objeto ExecAction

Objeto de scripting que representa una acción que ejecuta una operación de línea de comandos.

## <a name="members"></a>Miembros

El **objeto ExecAction** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto ExecAction** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**Argumentos**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | Lectura/escritura<br/> | Obtiene o establece los argumentos asociados a la operación de línea de comandos.<br/>                                                 |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | Lectura/escritura<br/> | Se hereda del [**objeto Action.**](action.md) Obtiene o establece el identificador de la acción.<br/>                         |
| [**Ruta de acceso**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | Lectura/escritura<br/> | Obtiene o establece la ruta de acceso a un archivo ejecutable.<br/>                                                                           |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | Solo lectura<br/>  | Se hereda del [**objeto Action.**](action.md) Obtiene el tipo de la acción.<br/>                                       |
| [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | Lectura/escritura<br/> | Obtiene o establece el directorio que contiene el archivo ejecutable o los archivos que usa el archivo ejecutable.<br/> |



 

## <a name="remarks"></a>Comentarios

Si se usan variables de entorno en las propiedades [**Path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)o [**WorkingDirectory,**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) los valores de las variables de entorno se almacenan en caché y se usan cuando se inicia el Taskeng.exe (el motor de tareas). El motor de tareas no usará los cambios en las variables de entorno que se producen después de iniciar el motor de tareas.

Esta acción realiza una operación de línea de comandos. Por ejemplo, la acción podría ejecutar un script o iniciar un archivo ejecutable.

Al leer o escribir XML, se especifica una acción de ejecución en el elemento [**Exec**](taskschedulerschema-exec-actiongroup-element.md) del Programador de tareas esquema.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea [Ejemplo de desencadenador de tiempo (scripting).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





