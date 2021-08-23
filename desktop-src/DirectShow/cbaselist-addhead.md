---
description: El método AddHead inserta otra lista al frente de esta lista.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: Método CBaseList.AddHead (Wxlist.h)
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
ms.openlocfilehash: fa8108af5f779bea4c1a1e756ab018ed9c902d3e516556c42b7899f442cb7704
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814325"
---
# <a name="cbaselistaddhead-method"></a>Método CBaseList.AddHead

El `AddHead` método inserta otra lista al frente de esta lista.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Plist* 
</dt> <dd>

Puntero a la lista de elementos que se agregarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

Si se produce un error en el método , es posible que se hayan agregado algunos elementos a la lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




