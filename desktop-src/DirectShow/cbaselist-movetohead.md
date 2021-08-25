---
description: El método MoveToHead divide la lista e inserta la parte final en la parte superior de otra lista.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Método CBaseList.MoveToHead (Wxlist.h)
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
ms.openlocfilehash: 18133107a3c8038780662bc39c8bd621c8b2c445a6e1e930f8fbfc015807e9fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928685"
---
# <a name="cbaselistmovetohead-method"></a>Método CBaseList.MoveToHead

El `MoveToHead` método divide la lista e inserta la parte final en la parte superior de otra lista.

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

*Plist* 
</dt> <dd>

Puntero a otra lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

Este método divide la lista antes de la posición especificada por el *parámetro pos.* La parte principal permanece en la lista. La parte final se inserta en la parte superior de la otra lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




