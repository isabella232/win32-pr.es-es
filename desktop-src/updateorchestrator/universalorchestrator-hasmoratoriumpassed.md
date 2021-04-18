---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Consulta a universal Orchestrator para determinar si se ha superado el período posterior a OOBE.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "105720776"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a>IUniversalOrchestrator:: HasMoratoriumPassed (método)

> [!NOTE] 
> Esta API pertenece a la API de orquestador universal.

Permite a los clientes determinar si el orquestador universal funciona inmediatamente después de la nueva experiencia del dispositivo, lo que limita los intentos de trabajo para minimizar la interrupción del usuario. 

## <a name="syntax"></a>Sintaxis

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a>Parámetros

`callerIdentifier`

Cadena única que identifica todas las llamadas de este cliente específico.

`hasMoratoriumPassed`

Parámetro de salida que almacena el resultado de la consulta.

## <a name="return-value"></a>Valor devuelto
Si este método se ejecuta correctamente, devuelve **S_OK**.  De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

| Requisito | Versión |
|---|---|
| Cliente mínimo compatible | Windows 10 1903 |
|   |   |



 

 



