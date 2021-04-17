---
description: El método CheckMediaType determina si el PIN acepta un tipo de medio específico.
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Método CBasePin. CheckMediaType (Amfilter. h)
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
ms.openlocfilehash: e203851a44a5468567e75ee8c0cc955f8ad0278a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661234"
---
# <a name="cbasepincheckmediatype-method"></a>CBasePin. CheckMediaType, método

El `CheckMediaType` método determina si el PIN acepta un tipo de medio específico.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*p.p.* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el tipo de medio propuesto es aceptable. De lo contrario, devuelve S \_ false o un código de error.

## <a name="remarks"></a>Observaciones

La clase derivada debe reemplazar este método virtual puro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




