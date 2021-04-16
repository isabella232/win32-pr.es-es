---
description: Este operador multiplica un tiempo de referencia por un valor.
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: Método COARefTime. Operator * (Ctlutil. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671247"
---
# <a name="coareftimeoperator-method"></a>COARefTime. Operator ( \* método)

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

Devuelve un nuevo objeto **COARefTime** igual al producto de este objeto y **l**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COARefTime**](coareftime.md)
</dt> </dl>

 

 




