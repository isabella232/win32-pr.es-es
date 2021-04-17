---
description: 'El método Receive recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior. Este método invalida el método CTransformFilter:: Receive.'
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: Método CVideoTransformFilter. Receive (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc33773a31a7c9ddfd7adb0f3fb20f8fcf6d520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680313"
---
# <a name="cvideotransformfilterreceive-method"></a>CVideoTransformFilter. Receive (método)

El `Receive` método recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior. Este método invalida el método [**CTransformFilter:: Receive**](ctransformfilter-receive.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) en el ejemplo de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                             | Descripción                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | El filtro de nivel superior debe dejar de enviar ejemplos.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                                         |



 

## <a name="remarks"></a>Observaciones

Este método llama a [**CVideoTransformFilter:: ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) para determinar si debe proporcionar este ejemplo o simplemente descartarlo. Si **ShouldSkipFrame** devuelve **false** (lo que indica que se debe entregar el ejemplo), el método hace lo siguiente:

1.  Llama a [**CTransformFilter:: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) para preparar el ejemplo de salida
2.  Llama a [**CTransformFilter:: transform**](ctransformfilter-transform.md) para procesar el ejemplo de entrada. Este método es virtual puro y debe implementarse en la clase derivada.
3.  Llama a [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md) para proporcionar el ejemplo de salida.

Además, este método comprueba los cambios de formato en el ejemplo de entrada o salida llamando a [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype). Si hay un cambio de formato, el método establece el tipo de conexión en el PIN correspondiente. Antes de establecer el nuevo tipo, llama a **StopStreaming**. Después de establecer el nuevo tipo, llama a **StartStreaming**. La clase derivada puede usar estos métodos para actualizar su estado interno. La clase derivada también podría necesitar comprobar el nuevo formato en su método de **transformación** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




