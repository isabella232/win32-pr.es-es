---
description: El método Receive recibe un ejemplo multimedia, lo procesa y lo entrega al filtro de nivel inferior.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: Método CTransInPlaceFilter. Receive (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e7a1f87617b59c31139cb3d857c83d4470fd709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661021"
---
# <a name="ctransinplacefilterreceive-method"></a>CTransInPlaceFilter. Receive (método)

El `Receive` método recibe un ejemplo multimedia, lo procesa y lo entrega al filtro de nivel inferior.

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

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) en el ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                  | Descripción                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto<br/>          |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Error inesperado<br/> |



 

## <a name="remarks"></a>Observaciones

El PIN de entrada del filtro llama a este método cuando recibe un ejemplo. El filtro llama al método de [**transformación**](ctransinplacefilter-transform.md) , que la clase derivada debe implementar. El método **Transform** procesa los datos. Si el filtro usa solo un asignador, pasa *pSample* directamente al método de **transformación** . De lo contrario, copia *pSample* y pasa la copia.

Si el método **Transform** devuelve S \_ false, el `Receive` método quita el ejemplo. En el primer ejemplo quitado, el filtro envía un evento de [**\_ \_ cambio de calidad EC**](ec-quality-change.md) al administrador de gráficos de filtro. De lo contrario, si el método de **transformación** devuelve S \_ correcto, el filtro entrega el ejemplo de salida. Para ello, llama al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el PIN de entrada de nivel inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




