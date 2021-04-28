---
description: 'Método CBasePin.CheckMediaType: el método CheckMediaType determina si el pin acepta un tipo de medio específico.'
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Método CBasePin.CheckMediaType (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afe39f3a7aac155f3cc87fa6d58f402043861d1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099403"
---
# <a name="cbasepincheckmediatype-method"></a>Método CBasePin.CheckMediaType

El `CheckMediaType` método determina si el pin acepta un tipo de medio específico.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el tipo de medio propuesto es aceptable. De lo contrario, devuelve S \_ FALSE o un código de error.

## <a name="remarks"></a>Comentarios

La clase derivada debe invalidar este método virtual puro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




