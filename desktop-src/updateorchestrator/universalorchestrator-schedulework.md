---
title: IUniversalOrchestrator::ScheduleWork
description: Llama al orquestador universal para programar el trabajo
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 456df8f975114f7bdf750a0449f3bd98efcc3b2e
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "105720778"
---
# <a name="iuniversalorchestratorschedulework-method"></a>IUniversalOrchestrator:: Scheduled (método)

> [!NOTE] 
> Esta API pertenece a la API de orquestador universal.

Permite a los clientes informar a universal Orchestrator de que el trabajo está pendiente y proporcionar un archivo binario al que llamará universal Orchestrator para realizar la actualización en un momento posterior.

El archivo binario de devolución de llamada debe estar firmado con un certificado de Microsoft válido, y el llamador debe invocar la llamada de programación desde el contexto del sistema.

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

Ruta de acceso completa al archivo binario de devolución de llamada que va a invocar el orquestador universal para realizar el trabajo.

`startArg`

Se solicitan los parámetros que se van a pasar al binario de devolución de llamada para indicar que se inicia.

`pauseArg`

*(opcional)* Parámetros que se van a pasar al binario de devolución de llamada para indicar que se solicita la pausa.

## <a name="return-value"></a>Valor devuelto
Si este método se ejecuta correctamente, devuelve **S_OK**.  De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

| Requisito | Versión |
|---|---|
| Cliente mínimo compatible | Windows 10 1903 |
|   |   |



 

 



