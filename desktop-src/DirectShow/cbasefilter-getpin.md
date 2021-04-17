---
description: El método GetPin recupera un PIN. La clase CEnumPins llama a este método para enumerar los PIN del filtro.
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: Método CBaseFilter. GetPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bb8341bfd86b96a7358fb23036b71844f77d17a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660712"
---
# <a name="cbasefiltergetpin-method"></a>CBaseFilter. GetPin, método

El método **GetPin** recupera un PIN. La clase [**CEnumPins**](cenumpins.md) llama a este método para enumerar los PIN del filtro.

## <a name="syntax"></a>Sintaxis


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*n* 
</dt> <dd>

Índice de base cero del PIN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al objeto [**CBasePin**](cbasepin.md) que implementa el código PIN.

## <a name="remarks"></a>Observaciones

Debe implementar este método virtual puro en la clase derivada. Devuelve un puntero al *n* pines en este filtro, indizado desde cero. Puede elegir un orden de indexación arbitrario, siempre que el orden sea fijo. Si el filtro agrega o elimina PIN o la ordenación cambia por algún otro motivo en tiempo de ejecución, llame al método [**CBaseFilter:: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




