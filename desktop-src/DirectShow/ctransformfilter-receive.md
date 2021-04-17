---
description: El método Receive recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: Método CTransformFilter. Receive (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67924bffc4d4d80b998e686d80d0e50afcd040ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661024"
---
# <a name="ctransformfilterreceive-method"></a>CTransformFilter. Receive (método)

El `Receive` método recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior.

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

El PIN de entrada del filtro llama a este método cuando recibe un ejemplo. Este método llama al método [**CTransformFilter:: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) , que prepara un nuevo ejemplo de salida. A continuación, llama al método [**CTransformFilter:: transform**](ctransformfilter-transform.md) , que la clase derivada debe implementar. El método **Transform** procesa los datos de entrada y genera datos de salida.

Si el método **Transform** devuelve S \_ false, el `Receive` método quita este ejemplo. En el primer ejemplo quitado, el filtro envía un evento de [**\_ \_ cambio de calidad EC**](ec-quality-change.md) al administrador de gráficos de filtro. De lo contrario, si el método de **transformación** devuelve S \_ correcto, el filtro entrega el ejemplo de salida. Para ello, llama al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el PIN de entrada de nivel inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




