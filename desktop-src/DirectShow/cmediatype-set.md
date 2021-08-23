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
ms.openlocfilehash: 0a317b23b4870ad6e68032ed23f846a81019be358974ebbe75e2a5859db71303
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585885"
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

## <a name="remarks"></a>Comentarios

Este método copia todo el tipo de medio de *cmtype*.

## <a name="requirements"></a>Requisitos

| Requisito                   | Value                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | Mtype.h (incluir Secuencias.h)                                                                                     |
| Biblioteca | Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 




