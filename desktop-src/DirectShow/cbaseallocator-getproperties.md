---
description: 'El método GetProperties recupera el número de búferes que va a crear el asignador y las propiedades del búfer. Este método implementa el método IMemAllocator:: GetProperties.'
ms.assetid: ccee4d69-52fc-4e3c-b6a4-787914708be4
title: Método CBaseAllocator. GetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abf143b11b6dd67fca6c87f9a31ce69f18951311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660610"
---
# <a name="cbaseallocatorgetproperties-method"></a>CBaseAllocator. GetProperties (método)

El `GetProperties` método recupera el número de búferes que va a crear el asignador y las propiedades del búfer. Este método implementa el método [**IMemAllocator:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProperties(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProps* 
</dt> <dd>

Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que recibe las propiedades de asignador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




