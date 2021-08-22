---
description: 'Constructor CBaseList.CBaseList(TCHAR \* , INT): método constructor.'
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Constructor CBaseList.CBaseList(TCHAR*, INT) (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5bd3462da5b8403f4db8f4727c0baa0a825e0db62b95216801300442d5cc393c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586275"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a>Constructor CBaseList.CBaseList(TCHAR, \* INT)

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero al nombre de la lista.

</dd> <dt>

*iItems* 
</dt> <dd>

Tamaño de la caché del nodo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para mejorar la eficacia, `CBaseList` la clase mantiene una caché de nodos de lista. Si sabe aproximadamente cuántos elementos contendrán la lista, use esta versión del constructor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




