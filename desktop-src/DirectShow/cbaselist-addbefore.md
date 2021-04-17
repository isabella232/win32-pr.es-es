---
description: El método AddBefore inserta una lista antes de la posición especificada.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Método CBaseList. AddBefore (Wxlist. h)
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
ms.openlocfilehash: 6a3c25b2dd545b3e6698404bf00f82d1086bfb81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660679"
---
# <a name="cbaselistaddbefore-method"></a>CBaseList. AddBefore, método

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

*pList* 
</dt> <dd>

Puntero a la lista que se va a insertar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true si es** correcto. De lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Los indicadores de posición existentes, incluido el especificado en el parámetro *pos* , siguen siendo válidos. Si se produce un error en el método, es posible que se hayan agregado algunos elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseList**](cbaselist.md)
</dt> </dl>

 

 




