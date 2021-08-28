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
ms.openlocfilehash: 0b734722371aa80e3c120dde3c6fb629785dfc6cdf9786c7f4ab1cbea87e5559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016983"
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
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




