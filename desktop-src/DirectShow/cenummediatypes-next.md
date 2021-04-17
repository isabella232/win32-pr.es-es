---
description: 'El método siguiente recupera un número especificado de tipos de medios. Este método implementa el método IEnumMediaTypes:: Next.'
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Método CEnumMediaTypes. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5eaa75a52f88539438cec58f024919577518e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660868"
---
# <a name="cenummediatypesnext-method"></a>CEnumMediaTypes. Next (método)

El `Next` método recupera un número especificado de tipos de medios. Este método implementa el método [**IEnumMediaTypes:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Next(
   ULONG         cMediaTypes,
   AM_MEDIA_TYPE **ppMediaTypes,
   ULONG         *pcFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

Número de tipos de medios que se van a recuperar.

</dd> <dt>

*ppMediaTypes* 
</dt> <dd>

Matriz de punteros a estructuras de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , de tamaño *cPins*.

</dd> <dt>

*pcFetched* 
</dt> <dd>

Puntero a una variable que recibe el número de tipos de medios que devuelve el método. Puede ser **null** si *cMediaTypes* es 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | No recuperó tantos tipos de medios como se solicitó.<br/>                       |
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | Correcto.<br/>                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Argumento no válido.<br/>                                                        |
| <dl> <dt>**\_puntero E**</dt> </dl>                  | Argumento de puntero **nulo** .<br/>                                               |
| <dl> <dt>**\_ \_ enumeración de VFW E no \_ \_ \_ sincronizada**</dt> </dl> | El estado del PIN ha cambiado y ahora es incoherente con el enumerador.<br/> |



 

## <a name="remarks"></a>Observaciones

Si el método se ejecuta correctamente, la matriz especificada por *ppMediaTypes* contiene punteros a \_ estructuras de tipo de medio am \_ . El número de estructuras es igual a *\* pcFetched*. Libere cada tipo de medio mediante una llamada a la función [**DeleteMediaType**](deletemediatype.md) .

Este método llama al método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) del PIN para recuperar los tipos de medios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




