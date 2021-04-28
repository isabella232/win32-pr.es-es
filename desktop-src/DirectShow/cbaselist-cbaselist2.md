---
description: 'Constructor CBaseList.CBaseList: método constructor.'
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Constructor CBaseList.CBaseList (Wxlist.h)
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
ms.openlocfilehash: 66aad24fe2d5176c684d4d78be27833e3be2f909
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096333"
---
# <a name="cbaselistcbaselist-constructor"></a>Constructor CBaseList.CBaseList

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero al nombre de la lista.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para mejorar la eficacia, `CBaseList` la clase mantiene una caché de nodos de lista. Esta versión del constructor usa un tamaño de caché predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Streams.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




