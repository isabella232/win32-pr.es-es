---
description: El método Next recupera un número especificado de tipos de medios. Este método implementa el método IEnumMediaTypes::Next.
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Método CEnumMediaTypes.Next (Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973887"
---
# <a name="cenummediatypesnext-method"></a>CEnumMediaTypes.Next (método)

El `Next` método recupera un número especificado de tipos de medios. Este método implementa el [**método IEnumMediaTypes::Next.**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next)

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

Número de tipos de medios que se recuperarán.

</dd> <dt>

*ppMediaTypes* 
</dt> <dd>

Matriz de punteros a [**estructuras \_ AM MEDIA \_ TYPE,**](/windows/win32/api/strmif/ns-strmif-am_media_type) de *tamaño cPins*.

</dd> <dt>

*pcFetched* 
</dt> <dd>

Puntero a una variable que recibe el número de tipos de medios devueltos por el método. Puede ser **NULL** si *cMediaTypes* es 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | No recuperó tantos tipos de medios como se solicitó.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Correcto.<br/>                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Argumento no válido.<br/>                                                        |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>                  | **Argumento de** puntero NULL.<br/>                                               |
| <dl> <dt>**VFW \_ E \_ ENUM \_ OUT \_ OF \_ SYNC**</dt> </dl> | El estado del pin ha cambiado y ahora es incoherente con el enumerador.<br/> |



 

## <a name="remarks"></a>Observaciones

Si el método se realiza correctamente, la matriz especificada por *ppMediaTypes* contiene punteros a estructuras \_ DE AM MEDIA \_ TYPE. El número de estructuras es igual a *\* pcFetched.* Libera cada tipo de medio llamando a [**la función DeleteMediaType.**](deletemediatype.md)

Este método llama al método [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) del pin para recuperar los tipos de medios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CEnumMediaTypes (clase)**](cenummediatypes.md)
</dt> </dl>

 

 




