---
title: Propiedad TaskSettings.Hidden
description: Para el scripting, obtiene o establece un valor booleano que indica que la tarea no estará visible en la interfaz de usuario.
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Propiedades ocultas Programador de tareas
- Propiedad oculta Programador de tareas , objeto TaskSettings
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
ms.openlocfilehash: b5a04ea67c6385e13235e10795dd2a7b250f2237f381ba2ca4f77a72832f9258
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857168"
---
# <a name="tasksettingshidden-property"></a>Propiedad TaskSettings.Hidden

Para el scripting, obtiene o establece un valor booleano que indica que la tarea no estará visible en la interfaz de usuario. Sin embargo, los administradores pueden invalidar esta configuración mediante el uso de un "modificador maestro" que hace que todas las tareas sean visibles en la interfaz de usuario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es True**, el valor indica que la tarea no estará visible en la interfaz de usuario. Si **es False**, la tarea estará visible en la interfaz de usuario. El valor predeterminado es **False**.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) del esquema Programador de tareas datos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





