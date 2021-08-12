---
description: El método Next recupera la siguiente posición de la lista.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Método CBaseList.Next (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d07030c046f3fe55178707af297542f383bfd5cf75f40169b5c93cfafa1c698b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658961"
---
# <a name="cbaselistnext-method"></a>CBaseList.Next (método)

El `Next` método recupera la siguiente posición de la lista.

## <a name="syntax"></a>Sintaxis


```C++
POSITION Next(
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

Devuelve el indicador de posición que sigue a la posición especificada por *pos*.

## <a name="remarks"></a>Observaciones

Si *pos* es la última posición de la lista, el método devuelve **NULL.** Si *pos* es **NULL,** el método devuelve la primera posición de la lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




