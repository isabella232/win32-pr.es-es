---
description: 'Método CBasePin.SetMediaType: el método SetMediaType establece el tipo de medio para la conexión.'
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Método CBasePin.SetMediaType (Amfilter.h)
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
ms.openlocfilehash: b61b6179aa6364ebddd940b8853e22d628463e56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095993"
---
# <a name="cbasepinsetmediatype-method"></a>Método CBasePin.SetMediaType

El `SetMediaType` método establece el tipo de medio para la conexión.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) que especifica el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Este método establece el formato para una conexión de pin. Antes de llamar a este método, el pin llama al método [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) para determinar si el tipo de medio es aceptable. Por lo tanto, se supone que el parámetro *pmt* es un tipo de medio aceptable.

En la clase base, este método establece la variable miembro [**CBasePin::m \_ mt**](cbasepin-m-mt.md) y devuelve S \_ OK. Una clase derivada puede invalidar este método si requiere notificación cuando se establece el tipo de medio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




