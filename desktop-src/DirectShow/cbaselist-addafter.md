---
description: El método AddAfter inserta una lista después de la posición especificada.
ms.assetid: c2a2e599-0a83-4eb0-aceb-c483f153ba7e
title: Método CBaseList.AddAfter (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28351e1e0762b8e45bc9bf2ba1fe3624c67339e9b8bcf59ec5a919850a853061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983515"
---
# <a name="cbaselistaddafter-method"></a>Método CBaseList.AddAfter

El `AddAfter` método inserta una lista después de la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddAfter(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Posición después de la cual se va a insertar la lista.

</dd> <dt>

*Plist* 
</dt> <dd>

Puntero a la lista que se insertará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

Los indicadores de posición existentes, incluido el especificado en el parámetro *pos,* siguen siendo válidos. Si se produce un error en el método, es posible que se hayan agregado algunos de los elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




