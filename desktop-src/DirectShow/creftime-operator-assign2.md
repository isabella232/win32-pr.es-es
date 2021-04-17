---
description: El operador = asigna una nueva hora de referencia. Este método usa el parámetro *ll* .
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: CRefTime. Operator = Method (Reftime. h)-ll (parámetro)
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
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187842"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a>CRefTime. Operator = Method (Reftime. h)-ll (parámetro)

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
| Encabezado  | Reftime. h (incluir streams. h)                                                                                   |
| Biblioteca | Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |



 

 




