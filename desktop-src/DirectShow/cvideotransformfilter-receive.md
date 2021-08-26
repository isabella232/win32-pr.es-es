---
description: El método Receive recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior. Este método invalida el método CTransformFilter::Receive.
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: Método CVideoTransformFilter.Receive (Vtrans.h)
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
ms.openlocfilehash: 6bce69d5f14a522f403eed54b56a340ab02316507766c0cc6d60ff897ec73541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998515"
---
# <a name="cvideotransformfilterreceive-method"></a>Método CVideoTransformFilter.Receive

El método recibe un ejemplo multimedia, lo procesa y entrega una muestra `Receive` de salida al filtro de nivel inferior. Este método invalida el [**método CTransformFilter::Receive.**](ctransformfilter-receive.md)

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

Puntero a la [**interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) en el ejemplo de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                             | Descripción                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El filtro ascendente debe dejar de enviar muestras.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                                         |



 

## <a name="remarks"></a>Comentarios

Este método llama [**a CVideoTransformFilter::ShouldSkipFrame para**](cvideotransformfilter-shouldskipframe.md) determinar si debe entregar este ejemplo o simplemente descartarlo. Si **ShouldSkipFrame** devuelve **FALSE** (que indica que se debe entregar el ejemplo), el método hace lo siguiente:

1.  Llama [**a CTransformFilter::InitializeOutputSample para**](ctransformfilter-initializeoutputsample.md) preparar el ejemplo de salida.
2.  Llama [**a CTransformFilter::Transform para**](ctransformfilter-transform.md) procesar el ejemplo de entrada. Este método es virtual puro y debe implementarse en la clase derivada.
3.  Llama [**a CBaseOutputPin::D eliver para**](cbaseoutputpin-deliver.md) entregar el ejemplo de salida.

Además, este método comprueba los cambios de formato en el ejemplo de entrada o salida, llamando a [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype). Si hay un cambio de formato, el método establece el tipo de conexión en el pin correspondiente. Antes de establecer el nuevo tipo, llama a **StopStreaming.** Después de establecer el nuevo tipo, llama **a StartStreaming.** La clase derivada puede usar estos métodos para actualizar su estado interno. Es posible que la clase derivada también tenga que comprobar el nuevo formato en su **método Transform.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CVideoTransformFilter (clase)**](cvideotransformfilter.md)
</dt> </dl>

 

 




