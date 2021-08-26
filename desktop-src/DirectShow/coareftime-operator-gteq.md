---
description: Este operador comprueba si una hora de referencia es menor o igual que otra.
ms.assetid: ae7449b7-d319-4e76-892f-0f9ae63ddf94
title: COARefTime.operator>= method (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6d19686fc2c904534f66882172db6bec52b4873a36104ce78d2d826a771978d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108475"
---
# <a name="coareftimeoperator-method"></a>COARefTime.operator>= method

Este operador comprueba si una hora de referencia es menor o igual que otra.

## <a name="syntax"></a>Sintaxis


```C++
BOOL operator>=(
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

Devuelve **TRUE** si este objeto es menor o igual que *rt*. De lo contrario, **devuelve FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COARefTime (clase)**](coareftime.md)
</dt> </dl>

 

 




