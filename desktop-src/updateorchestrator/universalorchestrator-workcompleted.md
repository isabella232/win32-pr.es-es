---
title: IUniversalOrchestrator::WorkCompleted
description: Llama a Universal Orchestrator para indicar que el trabajo ha finalizado
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 5094ae864b4df9a3dd53b90c3b7d099a206a0ad8db1d1176b603b5ba45ca8194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966100"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a>IUniversalOrchestrator::WorkCompleted (Método)

> [!NOTE] 
> Esta API pertenece a la API de Orquestador universal.

Permite a los clientes informar a Universal Orchestrator de que se ha completado el trabajo programado previamente y detener las devoluciones de llamada para realizar el trabajo hasta la siguiente llamada correcta a ScheduleWork.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a>Parámetros

`callerIdentifier`

Cadena única que identifica todas las llamadas desde este cliente específico.

`workCompleted`

**TRUE** si el trabajo se completó correctamente. De lo **contrario, false** si se ha intentado realizar el trabajo con error y se debe volver a intentar en el futuro. 

## <a name="return-value"></a>Valor devuelto
Si este método se realiza correctamente, devuelve **S_OK**.  De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

| Requisito | Versión |
|---|---|
| Cliente mínimo compatible | Windows 10 1903 |
|   |   |



 

 



