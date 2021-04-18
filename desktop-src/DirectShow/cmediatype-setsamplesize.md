---
description: El método SetSampleSize especifica un tamaño de muestra fijo o especifica que los ejemplos tienen un tamaño variable.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Método CMediaType. SetSampleSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0992afd0576c1039397e6ecaa2119a989283136e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680286"
---
# <a name="cmediatypesetsamplesize-method"></a>CMediaType. SetSampleSize, método

El `SetSampleSize` método especifica un tamaño de muestra fijo o especifica que los ejemplos tienen un tamaño variable.

## <a name="syntax"></a>Sintaxis


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SZ* 
</dt> <dd>

Tamaño de muestra, en bytes o cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el valor de *SZ* es cero, el tipo de medio usa tamaños de muestra variables. De lo contrario, el tamaño de la muestra se fija en *SZ* bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 




