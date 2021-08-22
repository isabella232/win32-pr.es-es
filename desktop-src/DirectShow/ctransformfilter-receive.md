---
description: El método Receive recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: Método CTransformFilter.Receive (Transfrm.h)
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
ms.openlocfilehash: 6a0c57cf6826274169a5984dd794e1ba9a5b8e78c7ffb774b00b05f16384e4a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953414"
---
# <a name="ctransformfilterreceive-method"></a>Método CTransformFilter.Receive

El método recibe un ejemplo multimedia, lo procesa y entrega un ejemplo `Receive` de salida al filtro de nivel inferior.

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
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El filtro ascendente debe dejar de enviar ejemplos.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                                         |



 

## <a name="remarks"></a>Comentarios

El pin de entrada del filtro llama a este método cuando recibe un ejemplo. Este método llama al [**método CTransformFilter::InitializeOutputSample,**](ctransformfilter-initializeoutputsample.md) que prepara un nuevo ejemplo de salida. A continuación, llama [**al método CTransformFilter::Transform,**](ctransformfilter-transform.md) que la clase derivada debe implementar. El **método Transform** procesa los datos de entrada y genera datos de salida.

Si el **método Transform** devuelve S \_ FALSE, el método quita este `Receive` ejemplo. En el primer ejemplo descartado, el filtro envía un evento [**EC \_ QUALITY \_ CHANGE**](ec-quality-change.md) al administrador de gráficos de filtros. De lo contrario, si **el método Transform** devuelve S \_ OK, el filtro entrega el ejemplo de salida. Para ello, llama al método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el pin de entrada de bajada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




