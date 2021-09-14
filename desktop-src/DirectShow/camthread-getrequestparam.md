---
description: El método GetRequestParam recupera la solicitud más reciente.
ms.assetid: f5bf4935-29ea-45b9-a57e-9fdcd9cde20a
title: Método CAMThread.GetRequestParam (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestParam
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dd6584123663bb36f1db4771fb3f86d7ac4f5cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160251"
---
# <a name="camthreadgetrequestparam-method"></a>Método CAMThread.GetRequestParam

El `GetRequestParam` método recupera la solicitud más reciente.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el valor del parámetro que se pasó más recientemente al [**método CAMThread::CallWorker.**](camthread-callworker.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




