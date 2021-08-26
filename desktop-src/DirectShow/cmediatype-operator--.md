---
description: Este operador comprueba la igualdad entre objetos CMediaType.
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: Método CMediaType.CMediaType::operator== (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93bc74338f994b967f313b7ed77529f9d90a8d01992b74cf4010f9aa51ab6a9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043663"
---
# <a name="cmediatypecmediatypeoperator-method"></a>CMediaType.CMediaType::operator== (método)

Este operador comprueba la igualdad entre [**objetos CMediaType.**](cmediatype.md)

## <a name="syntax"></a>Sintaxis


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Referencia al **objeto CMediaType** que se comparará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si *rt* es igual a este objeto. De lo contrario, **devuelve FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 




