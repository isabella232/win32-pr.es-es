---
description: El método activo notifica al pin que el filtro está activo ahora.
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Método CDynamicOutputPin. Active (Amfilter. h)
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
ms.openlocfilehash: 8f1765d0aa524c0dafd03a3fe4133af71e32fa70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671761"
---
# <a name="cdynamicoutputpinactive-method"></a>CDynamicOutputPin. Active (método)

El `Active` método notifica al pin que el filtro está activo ahora.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                            | Descripción                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                                                                                             |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Error. No se llamó a [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) .<br/> |



 

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBaseOutputPin:: Active**](cbaseoutputpin-active.md) . Restablece el evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) . Si el filtro propietario no ha llamado a **SetConfigInfo**, este método devuelve E \_ Fail.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




