---
description: Este operador agrega dos horas de referencia.
ms.assetid: 4dfc087a-ec4f-4a8a-8bd4-4da9e1699bcd
title: Método COARefTime. Operator + (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a6f5019c61d4c1baec47652db8842aa5085b675
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680599"
---
# <a name="coareftimeoperator-method"></a>COARefTime. Operator + (método)

Este operador agrega dos horas de referencia.

## <a name="syntax"></a>Sintaxis


```C++
COARefTime operator+(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RT* \[ CLI\]
</dt> <dd>

Referencia al objeto **COARefTime** que se va a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un nuevo objeto **COARefTime** igual a la suma de las horas de referencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COARefTime**](coareftime.md)
</dt> </dl>

 

 




