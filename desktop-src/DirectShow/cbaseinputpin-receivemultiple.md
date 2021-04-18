---
description: 'El método ReceiveMultiple recibe una matriz de ejemplos. Este método implementa el método IMemInputPin:: ReceiveMultiple.'
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Método CBaseInputPin. ReceiveMultiple (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5725b7d8b70c8f7c61eb44231812997a903ba41a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671711"
---
# <a name="cbaseinputpinreceivemultiple-method"></a>CBaseInputPin. ReceiveMultiple, método

El `ReceiveMultiple` método recibe una matriz de ejemplos. Este método implementa el método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSamples* 
</dt> <dd>

Dirección de una matriz de punteros [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) , de tamaño *nSamples*.

</dd> <dt>

*nSamples* 
</dt> <dd>

Número de muestras que se van a procesar.

</dd> <dt>

*nSamplesProcessed* 
</dt> <dd>

Puntero a una variable que recibe el número de muestras que se procesaron.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                                             | Descripción                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                    | Correcto.<br/>                                        |
| <dl> <dt>**S \_ false**</dt> </dl>                 | El PIN se está vaciando actualmente; se rechazó el ejemplo.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>               | Argumento de puntero **nulo** .<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de medio no válido.<br/>                             |
| <dl> <dt>**\_error de \_ tiempo de ejecución de VFW E \_**</dt> </dl>   | Se produjo un error en tiempo de ejecución.<br/>                      |
| <dl> <dt>**Estado de VFW \_ E \_ incorrecto \_**</dt> </dl>     | El PIN está detenido.<br/>                             |



 

## <a name="remarks"></a>Observaciones

Este método se comporta como el método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) , pero recibe una matriz de ejemplos. En la clase base, el método recorre en bucle la matriz y llama a **Receive** con cada ejemplo. Invalide esta función si el filtro puede procesar lotes de muestras de forma más eficaz que procesarlos de uno en uno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




