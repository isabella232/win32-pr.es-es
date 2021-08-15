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
ms.openlocfilehash: 12e59b434562e84c42228c16282620efe10866ea9dad85a4d62beb46f5a59e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688985"
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
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




