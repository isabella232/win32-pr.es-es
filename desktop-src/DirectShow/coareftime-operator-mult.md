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
ms.openlocfilehash: c62a4282f7a43ba3d7ba35daf81530f8b246be32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070083"
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

 

 




