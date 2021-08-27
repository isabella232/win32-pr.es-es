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
ms.openlocfilehash: f8dd593fe6ca550c55ffc1f769a303dd2d5cbf7a8d8c986be8a39278d7f334ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131295"
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

Matriz de punteros a [**estructuras \_ AM MEDIA \_ TYPE,**](/windows/win32/api/strmif/ns-strmif-am_media_type) de tamaño *cPins*.

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



 

## <a name="remarks"></a>Comentarios

Si el método se realiza correctamente, la matriz especificada por *ppMediaTypes* contiene punteros a estructuras \_ DE AM MEDIA \_ TYPE. El número de estructuras es igual a *\* pcFetched.* Liberar cada tipo de medio mediante una llamada a [**la función DeleteMediaType.**](deletemediatype.md)

Este método llama al método [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) del pin para recuperar los tipos de medios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CEnumMediaTypes (clase)**](cenummediatypes.md)
</dt> </dl>

 

 




