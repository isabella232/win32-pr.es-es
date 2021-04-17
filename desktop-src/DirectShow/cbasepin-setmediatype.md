---
description: El método SetMediaType establece el tipo de medio para la conexión.
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Método CBasePin. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 07ac736558cea12a16c695cf109c3d6283ce4a13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660943"
---
# <a name="cbasepinsetmediatype-method"></a>CBasePin. SetMediaType, método

El `SetMediaType` método establece el tipo de medio para la conexión.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*p.p.* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Este método establece el formato para una conexión de PIN. Antes de llamar a este método, el PIN llama al método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) para determinar si el tipo de medio es aceptable. Por lo tanto, se supone que el parámetro *PMT* es un tipo de medio aceptable.

En la clase base, este método establece la variable miembro [**CBasePin:: m \_ MT**](cbasepin-m-mt.md) y devuelve S \_ OK. Una clase derivada puede invalidar este método si requiere una notificación cuando se establece el tipo de medio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




