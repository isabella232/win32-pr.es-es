---
description: Este operador comprueba si una hora de referencia es menor que otra.
ms.assetid: 709fb861-a836-4a20-8c93-c0e8ab79f377
title: Método COARefTime. Operator< (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c61403b959f8b5ee19e9ba0d9cd0ab4db54c124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671252"
---
# <a name="coareftimeoperator-method"></a>COARefTime. Operator< método)

Este operador comprueba si una hora de referencia es menor que otra.

## <a name="syntax"></a>Sintaxis


```C++
BOOL operator<(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RT* \[ CLI\]
</dt> <dd>

Referencia al objeto **COARefTime** que se va a comparar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si este objeto es estrictamente menor que *RT*. De lo contrario, devuelve **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COARefTime**](coareftime.md)
</dt> </dl>

 

 




