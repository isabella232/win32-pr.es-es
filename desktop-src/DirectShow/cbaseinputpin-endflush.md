---
description: El método EndFlush finaliza una operación de vaciado. Implementa el método IPin::EndFlush.
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Método CBaseInputPin.EndFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403ee5aa100309084090dc241724067f9dd3aa5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173830"
---
# <a name="cbaseinputpinendflush-method"></a>Método CBaseInputPin.EndFlush

El `EndFlush` método finaliza una operación de vaciado. Implementa el [**método IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Este método establece la [**marca CBaseInputPin::m \_ bFlushing**](cbaseinputpin-m-bflushing.md) en **TRUE,** lo que permite que el método [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) acepte ejemplos.

La clase derivada debe invalidar este método y realizar los pasos siguientes:

1.  Liberar los datos almacenados en búfer y esperar a que se descarten todas las muestras en cola.
2.  Borre las notificaciones [**EC \_ COMPLETE**](ec-complete.md) pendientes.
3.  Llame al método de clase base.
4.  Llame [**a IPin::EndFlush en**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) los pines de entrada de nivel inferior. Si el pin aún no ha entregado ningún ejemplo multimedia de nivel inferior, puede omitir este paso. Si los pines de salida derivan de la clase [**CBaseOutputPin,**](cbaseoutputpin.md) puede llamar al método [**CBaseOutputPin::D eliverEndFlush.**](cbaseoutputpin-deliverendflush.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> </dl>

 

 




