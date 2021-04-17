---
description: El operador = asigna una nueva hora de referencia.
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: Método CRefTime. Operator = (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d93a57211c3bc7d787e68f70f36be868ff64449
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681059"
---
# <a name="creftimeoperator-method-reftimeh"></a>Método CRefTime. Operator = (Reftime. h)

El operador = asigna una nueva hora de referencia.

## <a name="syntax"></a>Sintaxis


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ll* 
</dt> <dd>

Nuevo tiempo de referencia, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia al objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Reftime. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




