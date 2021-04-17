---
description: Este operador resta una hora de referencia de otra.
ms.assetid: 5691cd76-0d25-45c0-bb58-6668abe1db01
title: COARefTime. Operator-Method (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e51ee8aaed69830a498d1d22cebdc3927987f045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670769"
---
# <a name="coareftimeoperator--method"></a>COARefTime. Operator-(método)

Este operador resta una hora de referencia de otra.

## <a name="syntax"></a>Sintaxis


```C++
COARefTime operator-(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RT* \[ CLI\]
</dt> <dd>

Referencia al objeto **COARefTime** que se va a restar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un nuevo objeto **COARefTime** igual a la diferencia de los tiempos de referencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COARefTime**](coareftime.md)
</dt> </dl>

 

 




