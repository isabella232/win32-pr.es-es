---
description: El método CMediaType.CMediaType::operator= (Mtype.h) sobrecarga el operador de asignación para copiar un tipo de medio.
ms.assetid: 28115548-97a5-426d-97cd-c5e759d8e39e
title: 'Método CMediaType.CMediaType::operator= (Mtype.h): parámetro cmtype'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16128d68d0b0443ae5cebf470b96f7e04bd63daedde7b41130bafca2692324ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916025"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh---cmtype-parameter"></a>Método CMediaType.CMediaType::operator= (Mtype.h): parámetro cmtype

Este operador sobrecarga el operador de asignación para copiar un tipo de medio.

## <a name="syntax"></a>Sintaxis


```C++
CMediaType& CMediaType::operator=(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cmtype* \[ Ref\]
</dt> <dd>

Referencia a un **objeto CMediaType.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia al objeto .

## <a name="requirements"></a>Requisitos

| Requisito                   | Value                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | Mtype.h (incluir Secuencias.h)                                                                                     |
| Biblioteca | Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 




