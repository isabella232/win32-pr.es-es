---
description: 'El método EndFlush finaliza una operación de vaciado. Implementa el método IPin:: EndFlush.'
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Método CBaseInputPin. EndFlush (Amfilter. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660345"
---
# <a name="cbaseinputpinendflush-method"></a>CBaseInputPin. EndFlush, método

El `EndFlush` método finaliza una operación de vaciado. Implementa el método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Este método establece la marca [**CBaseInputPin:: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) en **true**, lo que permite que el método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) acepte ejemplos.

La clase derivada debe invalidar este método y realizar los pasos siguientes:

1.  Libere los datos almacenados en búfer y espere a que se descarten todas las muestras en cola.
2.  Borre cualquier notificación de [**EC \_ completa**](ec-complete.md) pendiente.
3.  Llame al método de la clase base.
4.  Llame a [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en las clavijas de entrada de nivel inferior. Si el PIN no ha entregado todavía ningún ejemplo de multimedia en el nivel inferior, puede omitir este paso. Si los pin de salida derivan de la clase [**CBaseOutputPin**](cbaseoutputpin.md) , puede llamar al método [**eliverendflush de CBaseOutputPin::D**](cbaseoutputpin-deliverendflush.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




