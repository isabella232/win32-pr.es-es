---
description: El método SetSubtype especifica el subtipo.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Método CMediaType. SetSubtype (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6474777b1b2e91ce0b676fdc7dbd572d7c622f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670732"
---
# <a name="cmediatypesetsubtype-method"></a>CMediaType. SetSubtype, método

El `SetSubtype` método especifica el subtipo.

## <a name="syntax"></a>Sintaxis


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*psubtype* 
</dt> <dd>

Puntero a un **GUID** que especifica el subtipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 




