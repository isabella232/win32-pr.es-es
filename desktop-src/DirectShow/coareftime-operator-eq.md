---
description: Este operador comprueba la igualdad entre dos tiempos de referencia.
ms.assetid: a265f7c6-8334-4bb3-8cb7-c7918ebdf97a
title: Método COARefTime.operator== (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36951e2a2d0f82d73106f5b78ef9eb7e0b067c34dc4db3fd72521f48d8d4beb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831825"
---
# <a name="coareftimeoperator-method"></a>Método COARefTime.operator==

Este operador comprueba la igualdad entre dos tiempos de referencia.

## <a name="syntax"></a>Sintaxis


```C++
BOOL operator==(
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

Devuelve **TRUE** si los dos objetos son iguales. De lo contrario, **devuelve FALSE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COARefTime (clase)**](coareftime.md)
</dt> </dl>

 

 




