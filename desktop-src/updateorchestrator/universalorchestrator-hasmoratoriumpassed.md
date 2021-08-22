---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Consulta a Universal Orchestrator para determinar si se ha superado el período posterior a la OOBE.
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 61870e1bd57f54afded3f905da34ddc9198bcdb555c42adc4c799e08f2acf392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966142"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a>IUniversalOrchestrator::HasModoresPassed (método)

> [!NOTE] 
> Esta API pertenece a la API de Orquestador universal.

Permite a los clientes determinar si El orquestador universal funciona inmediatamente después de la nueva experiencia de configuración de dispositivo, lo que limita los intentos de trabajo para minimizar la interrupción del usuario. 

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
Si este método se realiza correctamente, devuelve **S_OK**.  De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

| Requisito | Versión |
|---|---|
| Cliente mínimo compatible | Windows 10 1903 |
|   |   |



 

 



