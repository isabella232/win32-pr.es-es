---
description: El método AddHeadI agrega un elemento al frente de la lista.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Método CBaseList.AddHeadI (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c1f22434aa2c927933c36ec496d5880ca8f3f673b314d7a8197079203757427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568125"
---
# <a name="cbaselistaddheadi-method"></a>Método CBaseList.AddHeadI

El `AddHeadI` método agrega un elemento al frente de la lista.

## <a name="syntax"></a>Sintaxis


```C++
POSITION AddHeadI(
   void *pObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pObj* 
</dt> <dd>

Puntero al elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor POSITION que indica la nueva posición de la cabeza.

## <a name="remarks"></a>Comentarios

Si se produce un error en el método , el valor devuelto es **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




