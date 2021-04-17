---
description: El método MoveToHead divide la lista e inserta la parte del final en el encabezado de otra lista.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Método CBaseList. MoveToHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80adec6c8e2f6d42b5cf2cabd3a83a4c3aededa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670928"
---
# <a name="cbaselistmovetohead-method"></a>CBaseList. MoveToHead, método

El `MoveToHead` método divide la lista e inserta la parte del final en el encabezado de otra lista.

## <a name="syntax"></a>Sintaxis


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Indicador de posición que marca la división en la lista.

</dd> <dt>

*pList* 
</dt> <dd>

Puntero a otra lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Este método divide la lista antes de la posición especificada por el parámetro *pos* . La parte del encabezado permanece en la lista. La parte del final se inserta en el encabezado de la otra lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseList**](cbaselist.md)
</dt> </dl>

 

 




