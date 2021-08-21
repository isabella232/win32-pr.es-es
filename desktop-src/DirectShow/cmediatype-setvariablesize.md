---
description: El método SetVariableSize especifica que los ejemplos no tienen un tamaño fijo.
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: Método CMediaType.SetVariableSize (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 118167d0068c058c925e5b63e2e951ff860917c40a5c3533daf9f02e6927649a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073969"
---
# <a name="cmediatypesetvariablesize-method"></a>Método CMediaType.SetVariableSize

El `SetVariableSize` método especifica que los ejemplos no tienen un tamaño fijo.

## <a name="syntax"></a>Sintaxis


```C++
void SetVariableSize();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método establece el **miembro bFixedSizeSamples** en **FALSE.** Las llamadas posteriores [**al método CMediaType::GetSampleSize**](cmediatype-getsamplesize.md) devuelven cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 




