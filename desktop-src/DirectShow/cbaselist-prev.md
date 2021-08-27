---
description: El método Prev recupera la posición anterior en la lista.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: Método CBaseList.Prev (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d04a63079e401b89286e10e927b540f40d04fc186546dbdbd4e31e8610fe617d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076605"
---
# <a name="cbaselistprev-method"></a>CBaseList.Prev (método)

El `Prev` método recupera la posición anterior en la lista.

## <a name="syntax"></a>Sintaxis


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Valor POSITION.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el indicador de posición anterior a la posición especificada en *pos*.

## <a name="remarks"></a>Comentarios

Si *pos* es la primera posición de la lista, el método devuelve **NULL.** Si *pos* es **NULL,** el método devuelve la última posición de la lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




