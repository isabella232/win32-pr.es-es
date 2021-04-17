---
description: Este operador divide una hora de referencia por un valor.
ms.assetid: fb2e2a4b-dc0b-42e3-86c7-8aa2c60daedc
title: COARefTime. Operator/Method (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator/
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e1e4d7b7adb881ac11988a2d2c46946ff6cddcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671228"
---
# <a name="coareftimeoperator-method"></a>COARefTime. Operator/(método)

Este operador divide una hora de referencia por un valor.

## <a name="syntax"></a>Sintaxis


```C++
COARefTime operator/(
   LONG l
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*l* 
</dt> <dd>

Divisor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un nuevo objeto **COARefTime** igual al cociente de este objeto y **l**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COARefTime**](coareftime.md)
</dt> </dl>

 

 




