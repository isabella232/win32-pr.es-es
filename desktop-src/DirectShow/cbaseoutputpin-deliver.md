---
description: El método Deliver entrega un ejemplo multimedia al pin de entrada conectado.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: Método CBaseOutputPin.Deliver (Amfilter.h)
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
ms.openlocfilehash: f6786e9e763af26619b2dc4f6abc25aa2fd9527d7278e7da02f6042908e56bdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341385"
---
# <a name="cbaseoutputpindeliver-method"></a>Método CBaseOutputPin.Deliver

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

Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>              |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El pin no está conectado.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método llama al [**método IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el pin de entrada. **Receive** puede bloquearse si [**el método IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) devuelve S \_ OK.

Libere el ejemplo después de llamar a este método. El pin de entrada puede contener un recuento de referencias en el ejemplo, por lo que no reutilice el ejemplo. Llame siempre al [**método CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) para obtener un nuevo ejemplo.

Mantenga la sección crítica del filtro antes de llamar a este método. De lo contrario, el pin podría desconectarse durante la llamada al método . Si el filtro usa un subproceso de trabajo para entregar ejemplos, mantenga la sección crítica cuando el filtro esté listo para entregar un ejemplo. De lo contrario, puede contener la sección crítica en el método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del filtro, donde el filtro procesa ejemplos.

Los subprocesos de trabajo pueden crear un posible interbloqueo. Cuando el subproceso contiene la sección crítica, puede esperar un cambio de estado en el filtro. Al mismo tiempo, es posible que el cambio de estado esté esperando a que se complete el subproceso. Para evitarlo, el código de cambio de estado debe indicar un evento que finaliza el subproceso y, a continuación, esperar a que el subproceso señale la finalización.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




