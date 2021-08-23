---
description: Este operador agrega dos veces de referencia y establece este objeto en el resultado.
ms.assetid: 6d29014b-0e31-497e-8326-e3fefc022227
title: Método COARefTime.operator+= (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dcb635e3026cec18aa5bea199b6712c15c6472d81e9b6707267d15d7afcfa6ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585565"
---
# <a name="coareftimeoperator-method"></a>Método COARefTime.operator+=

Este operador agrega dos veces de referencia y establece este objeto en el resultado.

## <a name="syntax"></a>Sintaxis


```C++
COARefTime& operator+=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Referencia al **objeto COARefTime que** se agregará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia al objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COARefTime (clase)**](coareftime.md)
</dt> </dl>

 

 




