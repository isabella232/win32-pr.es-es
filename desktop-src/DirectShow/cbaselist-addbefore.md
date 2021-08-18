---
description: El método AddBefore inserta una lista antes de la posición especificada.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Método CBaseList.AddBefore (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b4f85536b6a9372f164f596f96758a503096dbb0a5e5ed55adab42bc406b053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016973"
---
# <a name="cbaselistaddbefore-method"></a>Método CBaseList.AddBefore

El `AddBefore` método inserta una lista antes de la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Posición antes de la que se va a insertar la lista.

</dd> <dt>

*Plist* 
</dt> <dd>

Puntero a la lista que se insertará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente. De lo contrario, **devuelve FALSE**.

## <a name="remarks"></a>Comentarios

Los indicadores de posición existentes, incluido el especificado en el parámetro *pos,* siguen siendo válidos. Si se produce un error en el método , es posible que se hayan agregado algunos de los elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




