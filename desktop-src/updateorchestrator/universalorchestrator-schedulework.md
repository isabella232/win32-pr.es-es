---
title: IUniversalOrchestrator::ScheduleWork
description: Llama a Universal Orchestrator para programar el trabajo
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: bb2ecc67167e0651663856354a07ec86f985c664f1d2bccff98917adf72f054d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966102"
---
# <a name="iuniversalorchestratorschedulework-method"></a>IUniversalOrchestrator::ScheduleWork (método)

> [!NOTE] 
> Esta API pertenece a la API de Orquestador universal.

Permite a los clientes informar a Universal Orchestrator de que el trabajo está pendiente y proporcionar un archivo binario al que llamará Universal Orchestrator para realizar el trabajo de actualización más adelante.

El binario de devolución de llamada debe estar firmado con un certificado de Microsoft válido y el autor de la llamada debe invocar la llamada ScheduleWork desde el contexto system.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a>Parámetros

`callerIdentifier`

Cadena única que identifica todas las llamadas de este cliente específico.

`cmdLine`

Ruta de acceso completa al binario de devolución de llamada que invocará Universal Orchestrator para realizar el trabajo.

`startArg`

Parámetros que se pasan al binario de devolución de llamada para indicar que se solicita Start.

`pauseArg`

*(opcional)* Parámetros que se pasan al binario de devolución de llamada para indicar que se solicita pausar.

## <a name="return-value"></a>Valor devuelto
Si este método se realiza correctamente, devuelve **S_OK**.  De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

| Requisito | Versión |
|---|---|
| Cliente mínimo compatible | Windows 10 1903 |
|   |   |



 

 



