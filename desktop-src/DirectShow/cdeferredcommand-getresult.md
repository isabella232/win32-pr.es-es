---
description: El método GetResult recupera la lista de argumentos resultante, si existe.
ms.assetid: a2a8b17c-3dcf-4f59-89c3-f42070d2a8eb
title: Método CDeferredCommand.GetResult (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2176d6787bd520517cccbf484bdf6642921d499aaeb97c2917d64fa148323b66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076425"
---
# <a name="cdeferredcommandgetresult-method"></a>Método CDeferredCommand.GetResult

El `GetResult` método recupera la lista de argumentos resultante, si existe.

## <a name="syntax"></a>Sintaxis


```C++
VARIANT* GetResult();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a **un variant** que contiene la lista de argumentos del método, si existe.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDeferredCommand (clase)**](cdeferredcommand.md)
</dt> </dl>

 

 




