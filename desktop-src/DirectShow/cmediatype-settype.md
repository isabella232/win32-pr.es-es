---
description: El método SetType especifica el tipo principal.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: Método CMediaType. SetType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfcf6ca634bce92701eb89f26dcfb6bdfb51f698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671521"
---
# <a name="cmediatypesettype-method"></a>CMediaType. SetType, método

El `SetType` método especifica el tipo principal.

## <a name="syntax"></a>Sintaxis


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ptype* 
</dt> <dd>

Puntero a un **GUID** que especifica el tipo principal.

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

 

 




