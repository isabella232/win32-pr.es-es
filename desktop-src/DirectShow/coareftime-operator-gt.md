---
description: Este operador comprueba si una hora de referencia es mayor que otra.
ms.assetid: db281040-9bcf-41fc-95b4-5481ffc5061f
title: Método de> COARefTime.operator (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fd2da8b95345813682994f18a444f090c65c1f906219afb9a64bf5584679b194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652195"
---
# <a name="coareftimeoperator-method"></a>CoARefTime.operator> método

Este operador comprueba si una hora de referencia es mayor que otra.

## <a name="syntax"></a>Sintaxis


```C++
BOOL operator>(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Referencia al **objeto COARefTime** que se comparará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si este objeto es estrictamente mayor que *rt*. De lo contrario, **devuelve FALSE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COARefTime (clase)**](coareftime.md)
</dt> </dl>

 

 




