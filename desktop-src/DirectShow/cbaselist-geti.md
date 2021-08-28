---
description: El método GetI recupera el elemento en la posición especificada.
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: Método CBaseList.GetI (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f543a38c3394943e3ccb1eeb8bb97d29297a4ca230966940245a2f8a8c121b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087445"
---
# <a name="cbaselistgeti-method"></a>Método CBaseList.GetI

El `GetI` método recupera el elemento en la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Indicador de posición del elemento que se recuperará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al elemento.

## <a name="remarks"></a>Comentarios

Si *pos* es **NULL,** el método devuelve **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




