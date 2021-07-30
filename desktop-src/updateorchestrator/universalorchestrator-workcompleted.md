---
title: IUniversalOrchestrator::WorkCompleted
description: Llama a Universal Orchestrator para indicar que el trabajo ha finalizado
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: e36a3ba744df807abbebc6332ac8433010afd667
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991832"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a>IUniversalOrchestrator::WorkCompleted (método)

> [!NOTE] 
> Esta API pertenece a la API de Orquestador universal.

Permite a los clientes informar a Universal Orchestrator de que se ha completado el trabajo programado previamente y detener las devoluciones de llamada para realizar el trabajo hasta la siguiente llamada ScheduleWork correcta.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a>Parámetros

`callerIdentifier`

Cadena única que identifica todas las llamadas de este cliente específico.

`workCompleted`

**TRUE** si el trabajo se completó correctamente. De lo **contrario, false** si el intento de trabajo no se pudo realizar y se debe volver a intentar en el futuro. 

## <a name="return-value"></a>Valor devuelto
Si este método se realiza correctamente, devuelve **S_OK**.  De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

| Requisito | Versión |
|---|---|
| Cliente mínimo compatible | Windows 10 1903 |
|   |   |



 

 



