---
title: Elemento nivel (runLevelType)
description: Contiene un valor que especifica el nivel de contexto de seguridad para ejecutar la tarea.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- Programador de tareas del elemento nivel
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d374f5b9ad388f3ad0a626e1b99ecae96eeef1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359859"
---
# <a name="runlevel-runleveltype-element"></a>Elemento nivel (runLevelType)

Contiene un valor que especifica el nivel de contexto de seguridad para ejecutar la tarea. Puede especificar que se ejecute una tarea con privilegios mínimos o privilegios elevados. Un valor de 0 especifica que se ejecute la tarea con los privilegios más bajos y un valor de 1 especifica que se ejecute la tarea con privilegios elevados.

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

El elemento **nivel** se define mediante el tipo simple [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                  | Derivado de                                                           | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Entidad de seguridad (principalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad para una entidad de seguridad. Estas credenciales definen el contexto de seguridad en el que se ejecuta una tarea. <br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, consulte la [**propiedad nivel de IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).

Para el desarrollo de scripts, consulte [**principal. nivel**](principal-runlevel.md).

Si una tarea se registra mediante la **cuenta de \\ Administrador de Builtin** o las cuentas [LocalSystem](/windows/desktop/Services/localsystem-account) o [LocalService](/windows/desktop/Services/localservice-account) , se omite la propiedad [**nivel**](principal-runlevel.md) . El valor del atributo también se omitirá si el [control de cuentas de usuario](/windows/desktop/SecAuthZ/user-account-control) (UAC) está desactivado.

Si una tarea se registra mediante el grupo de **administradores** para el contexto de seguridad de la tarea, también debe establecer la propiedad [**nivel**](principal-runlevel.md) en "HighestAvailable" para ejecutar la tarea. Para obtener más información, vea [contextos de seguridad para tareas](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

