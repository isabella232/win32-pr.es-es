---
description: El método Receive recibe un ejemplo multimedia, lo procesa y lo entrega al filtro de nivel inferior.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: Método CTransInPlaceFilter.Receive (Transip.h)
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
ms.openlocfilehash: 390d0243631e4ac31da779ca01197500f1d3df18127a3b86f0cf1ea834283f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053465"
---
# <a name="ctransinplacefilterreceive-method"></a>Método CTransInPlaceFilter.Receive

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

Puntero a la [**interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                  | Descripción                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto<br/>          |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Error inesperado<br/> |



 

## <a name="remarks"></a>Comentarios

El pin de entrada del filtro llama a este método cuando recibe un ejemplo. El filtro llama al [**método Transform,**](ctransinplacefilter-transform.md) que la clase derivada debe implementar. El **método Transform** procesa los datos. Si el filtro usa un solo asignador, pasa *pSample* directamente al **método Transform.** De lo contrario, copia *pSample* y pasa la copia.

Si el **método Transform** devuelve S \_ FALSE, el método quita el `Receive` ejemplo. En el primer ejemplo descartado, el filtro envía un evento [**EC \_ QUALITY \_ CHANGE**](ec-quality-change.md) al administrador de gráficos de filtros. De lo contrario, si **el método Transform** devuelve S \_ OK, el filtro entrega el ejemplo de salida. Para ello, llama al método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el pin de entrada de bajada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 




