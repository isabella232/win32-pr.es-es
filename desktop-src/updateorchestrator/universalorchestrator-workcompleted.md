---
title: IUniversalOrchestrator::WorkCompleted
description: Llama al orquestador universal para indicar que el trabajo se ha completado
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 8d4a08e7f021811e59a182a8b726397476b78433
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "105720779"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a>IUniversalOrchestrator:: WorkCompleted (método)

> [!NOTE] 
> Esta API pertenece a la API de orquestador universal.

Permite a los clientes informar a la plataforma universal de que el trabajo programado anteriormente se ha completado y detener las devoluciones de llamada para que funcionen hasta la siguiente llamada de programación de trabajo correcta.

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

**True** si el trabajo se completó correctamente. En caso contrario, **false** si se produjo un error en el intento de trabajo y se debe volver a intentar en el futuro. 

## <a name="return-value"></a>Valor devuelto
Si este método se ejecuta correctamente, devuelve **S_OK**.  De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

| Requisito | Versión |
|---|---|
| Cliente mínimo compatible | Windows 10 1903 |
|   |   |



 

 



