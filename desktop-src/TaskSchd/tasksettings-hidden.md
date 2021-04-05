---
title: Propiedad TaskSettings. Hidden
description: En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea no estará visible en la interfaz de usuario.
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Propiedad Hidden Programador de tareas
- Propiedad Hidden Programador de tareas, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad Hidden
topic_type:
- apiref
api_name:
- TaskSettings.Hidden
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057a3d920ba70260d23ad13a5888072ab5b07767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803205"
---
# <a name="tasksettingshidden-property"></a>Propiedad TaskSettings. Hidden

En el caso de scripting, obtiene o establece un valor booleano que indica que la tarea no estará visible en la interfaz de usuario. Sin embargo, los administradores pueden invalidar esta configuración mediante el uso de un "modificador principal" que hace que todas las tareas sean visibles en la interfaz de usuario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true**, el valor indica que la tarea no estará visible en la interfaz de usuario. Si **es false**, la tarea estará visible en la interfaz de usuario. El valor predeterminado es **False**.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**oculto (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





