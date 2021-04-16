---
description: El método Deliver entrega un ejemplo multimedia al pin de entrada conectado.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: Método CBaseOutputPin. Deliver (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Deliver
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adc603e4cdd1f49e649264d2d82d6df0fb12569
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671509"
---
# <a name="cbaseoutputpindeliver-method"></a>CBaseOutputPin. Deliver (método)

El `Deliver` método entrega un ejemplo multimedia al pin de entrada conectado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Deliver(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>              |
| <dl> <dt>**VFW \_ E \_ no \_ conectada**</dt> </dl> | El PIN no está conectado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método llama al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el PIN de entrada. **Receive** puede bloquear si el método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) devuelve S \_ correctos.

Libere el ejemplo después de llamar a este método. El PIN de entrada puede contener un recuento de referencias en el ejemplo, por lo que no vuelva a usar el ejemplo. Llame siempre al método [**CBaseOutputPin:: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) para obtener un nuevo ejemplo.

Mantenga la sección crítica del filtro antes de llamar a este método. De lo contrario, el PIN podría desconectarse durante la llamada al método. Si el filtro usa un subproceso de trabajo para entregar ejemplos, mantenga la sección crítica cuando el filtro esté listo para entregar un ejemplo. De lo contrario, puede almacenar la sección crítica en el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del filtro, donde el filtro procesa los ejemplos.

Los subprocesos de trabajo pueden crear un posible interbloqueo. Cuando el subproceso contiene la sección crítica, podría esperar en un cambio de estado en el filtro. Al mismo tiempo, el cambio de estado podría estar esperando a que el subproceso se complete. Para evitar esto, el código de cambio de Estado debe señalar un evento que termine el subproceso y, a continuación, esperar a que el subproceso señale la finalización.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




