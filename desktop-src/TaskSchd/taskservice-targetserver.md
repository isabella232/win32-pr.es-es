---
title: Propiedad TaskService.TargetServer
description: Para el scripting, obtiene el nombre del equipo que ejecuta el Programador de tareas al que está conectado el usuario.
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- Propiedad TargetServer Programador de tareas
- Propiedad TargetServer Programador de tareas , objeto TaskService
- Objeto TaskService Programador de tareas propiedad , TargetServer
topic_type:
- apiref
api_name:
- TaskService.TargetServer
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79f68dfaf5d6000ad88dca9001102056eb349601630364105526ea0d29a8bf46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080295"
---
# <a name="taskservicetargetserver-property"></a>Propiedad TaskService.TargetServer

Para el scripting, obtiene el nombre del equipo que ejecuta el Programador de tareas al que está conectado el usuario.

## <a name="syntax"></a>Syntax


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a>Valor de propiedad

Nombre del equipo que ejecuta el servicio Programador de tareas al que está conectado el usuario.

## <a name="remarks"></a>Comentarios

Esta propiedad devuelve una cadena vacía cuando el usuario pasa una dirección IP, Localhost o "." como parámetro, y devuelve el nombre del equipo que ejecuta el servicio Programador de tareas cuando el usuario no pasa ningún valor de parámetro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





