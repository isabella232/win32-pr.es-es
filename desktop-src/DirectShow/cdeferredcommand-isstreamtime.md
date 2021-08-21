---
description: El método IsStreamTime especifica si el comando se va a ejecutar en tiempo de transmisión o en tiempo de presentación.
ms.assetid: 4fb315a4-1bc6-49c8-a47f-0a8a46f3f790
title: Método CDeferredCommand.IsStreamTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.IsStreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82c541220a2b89ecdd23e4676175f4c7b2aacd93aac008546349b38e7bc2455a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657208"
---
# <a name="cdeferredcommandisstreamtime-method"></a>Método CDeferredCommand.IsStreamTime

El método especifica si el comando se va a ejecutar en tiempo `IsStreamTime` de transmisión o en tiempo de presentación.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsStreamTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se establece en stream time; de lo contrario, **devuelve FALSE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDeferredCommand (clase)**](cdeferredcommand.md)
</dt> </dl>

 

 




