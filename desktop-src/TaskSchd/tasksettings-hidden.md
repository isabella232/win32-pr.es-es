---
title: Propiedad TaskSettings.Hidden
description: Para el scripting, obtiene o establece un valor booleano que indica que la tarea no estará visible en la interfaz de usuario.
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Propiedades ocultas Programador de tareas
- Propiedad hidden Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad Hidden
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968539"
---
# <a name="tasksettingshidden-property"></a>Propiedad TaskSettings.Hidden

Para el scripting, obtiene o establece un valor booleano que indica que la tarea no estará visible en la interfaz de usuario. Sin embargo, los administradores pueden invalidar esta configuración mediante el uso de un "modificador maestro" que hace que todas las tareas sean visibles en la interfaz de usuario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es True**, el valor indica que la tarea no estará visible en la interfaz de usuario. Si **es False**, la tarea estará visible en la interfaz de usuario. El valor predeterminado es **False**.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) del esquema Programador de tareas datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





