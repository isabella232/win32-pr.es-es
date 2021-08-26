---
description: Este operador multiplica un tiempo de referencia por un valor.
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: Método COARefTime.operator* (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator*
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57060f3b0436422c34ba947c0025cc6796d534e16ff64be029e68ab140faa4af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079355"
---
# <a name="coareftimeoperator-method"></a>Método COARefTime.operator \*

Este operador multiplica un tiempo de referencia por un valor.

## <a name="syntax"></a>Sintaxis


```C++
COARefTime operator*(
   LONG l
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*l* 
</dt> <dd>

Multiplicador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un nuevo **objeto COARefTime** igual al producto de este objeto y **l**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COARefTime (clase)**](coareftime.md)
</dt> </dl>

 

 




