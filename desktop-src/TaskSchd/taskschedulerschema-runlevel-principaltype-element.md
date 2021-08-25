---
title: Elemento RunLevel (runLevelType)
description: Contiene un valor que especifica el nivel de contexto de seguridad para ejecutar la tarea.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- Elemento RunLevel Programador de tareas
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 143db96de30e647c67abadc2a9fb4384ae9784604b9c679efd9de5fd2157f923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991095"
---
# <a name="runlevel-runleveltype-element"></a>Elemento RunLevel (runLevelType)

Contiene un valor que especifica el nivel de contexto de seguridad para ejecutar la tarea. Puede especificar para ejecutar una tarea con privilegios mínimos o privilegios elevados. Un valor de 0 especifica para ejecutar la tarea con privilegios más bajos y un valor de 1 especifica para ejecutar la tarea con privilegios elevados.

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

El tipo simple [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) define el elemento **RunLevel.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                  | Derivado de                                                           | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Principal (principalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad de una entidad de seguridad. Estas credenciales definen el contexto de seguridad en el que se ejecuta una tarea. <br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea Propiedad RunLevel de IPrincipal.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel)

Para el desarrollo de scripts, [**vea Principal.RunLevel**](principal-runlevel.md).

Si una tarea se registra con la cuenta **\\ de** administrador integrada o las cuentas [LocalSystem](/windows/desktop/Services/localsystem-account) o [LocalService,](/windows/desktop/Services/localservice-account) se omite la propiedad [**RunLevel.**](principal-runlevel.md) El valor del atributo también se omitirá si [el Control de cuentas](/windows/desktop/SecAuthZ/user-account-control) de usuario (UAC) está desactivado.

Si una tarea se  registra mediante el grupo Administradores para el contexto de seguridad de la tarea, también debe establecer la propiedad [**RunLevel**](principal-runlevel.md) en "HighestAvailable" para ejecutar la tarea. Para obtener más información, vea [Contextos de seguridad para tareas](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

