---
description: 'Método CBasePin.GetMediaType: el método GetMediaType recupera un tipo de medio preferido, por valor de índice.'
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Método CBasePin.GetMediaType (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 186f2eddbedf4eb0565a4ca66ff4ed7e5b080090
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099373"
---
# <a name="cbasepingetmediatype-method"></a>Método CBasePin.GetMediaType

El `GetMediaType` método recupera un tipo de medio preferido, por valor de índice.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iPosition* 
</dt> <dd>

Valor de índice de base cero.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) que recibe el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la tabla siguiente.



| Código devuelto                                                                                            | Descripción                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Correcto.<br/>              |
| <dl> <dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt> </dl> | Índice fuera del intervalo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Índice menor que cero.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>           | error inesperado.<br/>     |



 

## <a name="remarks"></a>Comentarios

En la lista de tipos de medios preferidos del pin, este método devuelve el tipo con un valor de índice *de iPosition*. La [**clase CEnumMediaTypes**](cenummediatypes.md) llama a este método para enumerar los tipos de medios preferidos.

La clase base devuelve E \_ UNEXPECTED. Invalide este método en la clase derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




