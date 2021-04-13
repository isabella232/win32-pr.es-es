---
title: Propiedad TaskService. TargetServer
description: En el caso de scripting, obtiene el nombre del equipo que está ejecutando el servicio Programador de tareas al que está conectado el usuario.
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- Programador de tareas de la propiedad TargetServer
- Programador de tareas de la propiedad TargetServer, objeto TaskService
- Programador de tareas de objeto TaskService, propiedad TargetServer
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
ms.openlocfilehash: ba4347915fae57585716a64a6a4ca549ccc1c299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535470"
---
# <a name="taskservicetargetserver-property"></a>Propiedad TaskService. TargetServer

En el caso de scripting, obtiene el nombre del equipo que está ejecutando el servicio Programador de tareas al que está conectado el usuario.

## <a name="syntax"></a>Sintaxis


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a>Valor de propiedad

Nombre del equipo que ejecuta el servicio Programador de tareas al que está conectado el usuario.

## <a name="remarks"></a>Observaciones

Esta propiedad devuelve una cadena vacía cuando el usuario pasa una dirección IP, localhost o '. ' como parámetro, y devuelve el nombre del equipo que ejecuta el servicio de Programador de tareas cuando el usuario no pasa ningún valor de parámetro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





