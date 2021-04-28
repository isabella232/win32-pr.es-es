---
description: 'Método CDynamicOutputPin.Active: el método Active notifica al pin que el filtro ahora está activo.'
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Método CDynamicOutputPin.Active (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d9544c0fd125146b10f008565fcfbe330d18de1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099333"
---
# <a name="cdynamicoutputpinactive-method"></a>Método CDynamicOutputPin.Active

El `Active` método notifica al pin que el filtro ahora está activo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                            | Descripción                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                                                                                             |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Error. [**No se llamó a CDynamicOutputPin::SetConfigInfo.**](cdynamicoutputpin-setconfiginfo.md)<br/> |



 

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBaseOutputPin::Active.**](cbaseoutputpin-active.md) Restablece el evento [**CDynamicOutputPin::m \_ hStopEvent.**](cdynamicoutputpin-m-hstopevent.md) Si el filtro propietario no ha llamado a **SetConfigInfo**, este método devuelve E \_ FAIL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




