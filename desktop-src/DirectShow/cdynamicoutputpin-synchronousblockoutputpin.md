---
description: El método SynchronousBlockOutputPin bloquea el pin; no devuelve hasta que se bloquea el pin.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Método CDynamicOutputPin.SynchronousBlockOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fff1a0a1f093b97d07c74d7916ef2a7511d0e16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062502"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a>Método CDynamicOutputPin.SynchronousBlockOutputPin

El `SynchronousBlockOutputPin` método bloquea el pin; no vuelve hasta que se bloquea.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                                                    | Descripción                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Correcto.<br/>                                      |
| <dl> <dt>**EL PIN \_ DE VFW E \_ YA \_ ESTÁ \_ BLOQUEADO**</dt> </dl>                   | El pin ya está bloqueado en otro subproceso.<br/>     |
| <dl> <dt>**EL PIN \_ DE VFW E \_ YA ESTÁ BLOQUEADO EN ESTE \_ \_ \_ \_ \_ SUBPROCESO**</dt> </dl> | El pin ya está bloqueado en el subproceso que realiza la llamada.<br/> |



 

## <a name="remarks"></a>Observaciones

No llame a este método desde el subproceso de streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




