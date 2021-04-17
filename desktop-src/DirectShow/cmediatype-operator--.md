---
description: Este operador comprueba la igualdad entre los objetos CMediaType.
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: 'CMediaType. CMediaType:: Operator = = (método, mtype. h)'
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
ms.openlocfilehash: 79631415ce562f1cf3d7251e1f325960f5baa28b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690680"
---
# <a name="cmediatypecmediatypeoperator-method"></a>CMediaType. CMediaType:: Operator = = (método)

Este operador comprueba la igualdad entre los objetos [**CMediaType**](cmediatype.md) .

## <a name="syntax"></a>Sintaxis


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RT* \[ CLI\]
</dt> <dd>

Referencia al objeto **CMediaType** que se va a comparar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si *RT* es igual a este objeto. De lo contrario, devuelve **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 




