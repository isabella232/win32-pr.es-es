---
description: El método CMediaType.Set (Mtype.h) establece el tipo de medio de otro tipo de medio. El método usa el parámetro "cmtype".
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: 'Método CMediaType.Set (Mtype.h): parámetro cmtype [ref]'
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362499"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a>Método CMediaType.Set (Mtype.h): parámetro cmtype [ref]

El `Set` método establece el tipo de medio de otro tipo de medio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cmtype* \[ Ref\]
</dt> <dd>

Referencia a un [**objeto CMediaType.**](cmediatype.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Este método copia todo el tipo de medio de *cmtype*.

## <a name="requirements"></a>Requisitos

| Requisito                   | Value                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | Mtype.h (incluir Secuencias.h)                                                                                     |
| Biblioteca | Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 




