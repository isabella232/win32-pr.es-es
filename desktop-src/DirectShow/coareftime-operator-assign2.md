---
description: El operador asigna una nueva hora de referencia y usa el parámetro "rt [ref]".
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: 'Método COARefTime.operator= (Ctlutil.h): parámetro rt [ref]'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1a1e4c9482c187db7d5d5377535763b9fbab126b2153e0efa56bc341b402b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103165"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a>Método COARefTime.operator= (Ctlutil.h): parámetro rt [ref]

Este operador asigna una nueva hora de referencia.

## <a name="syntax"></a>Sintaxis


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Referencia a un [**valor REFERENCE \_ TIME**](reference-time.md) que especifica el nuevo tiempo de referencia en unidades de 100 nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia al objeto .

## <a name="requirements"></a>Requisitos

| Requisito                    | Value                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | Ctlutil.h (incluir Secuencias.h)                                                                                   |
| Biblioteca | Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**COARefTime (clase)**](coareftime.md)
</dt> </dl>

 

 




