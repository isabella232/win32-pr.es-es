---
description: El método AddHead inserta otra lista al principio de esta lista.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: Método CBaseList. AddHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a262f2bcfb7c40671fd472ecd7d3f887b1db4224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670943"
---
# <a name="cbaselistaddhead-method"></a>CBaseList. AddHead, método

El `AddHead` método inserta otra lista al principio de esta lista.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pList* 
</dt> <dd>

Puntero a la lista de elementos que se van a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Si se produce un error en el método, es posible que algunos elementos se hayan agregado a la lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseList**](cbaselist.md)
</dt> </dl>

 

 




