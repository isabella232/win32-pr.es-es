---
description: El método CMediaType. set (mtype. h) establece el tipo de medio desde otro tipo de medio. El método usa el parámetro ' cmtype '.
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: Método CMediaType. set (mtype. h)-cmtype [Ref] parámetro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bf14132660045afbd171173a38d3ea320ba1aa
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105670277"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a>Método CMediaType. set (mtype. h)-cmtype [Ref] parámetro

El `Set` método establece el tipo de medio desde otro tipo de medio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cmtype* \[ CLI\]
</dt> <dd>

Referencia a un objeto [**CMediaType**](cmediatype.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Este método copia todo el tipo de medio de *cmtype*.

## <a name="requirements"></a>Requisitos

| Requisito                   | Value                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | Mtype. h (incluir streams. h)                                                                                     |
| Biblioteca | Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 




