---
description: Este operador agrega dos tiempos de referencia.
ms.assetid: 4dfc087a-ec4f-4a8a-8bd4-4da9e1699bcd
title: Método COARefTime.operator+ (Ctlutil.h)
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
ms.openlocfilehash: 348151b4bb7dc7cca6578755e10934364ba59b8ac5447c0bce4b5240483e7fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954344"
---
# <a name="coareftimeoperator-method"></a>Método COARefTime.operator+

Este operador agrega dos tiempos de referencia.

## <a name="syntax"></a>Sintaxis


```C++
COARefTime operator+(
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

Devuelve un nuevo **objeto COARefTime** igual a la suma de los tiempos de referencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COARefTime (clase)**](coareftime.md)
</dt> </dl>

 

 




