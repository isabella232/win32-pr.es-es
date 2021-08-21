---
description: El método AddTailI agrega un elemento al final de la lista.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: Método CBaseList.AddTailI (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3317877bfa67d2d39d469882e0b12b9fd79a923873022a51ee48712fc772743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659131"
---
# <a name="cbaselistaddtaili-method"></a>Método CBaseList.AddTailI

El `AddTailI` método agrega un elemento al final de la lista.

## <a name="syntax"></a>Sintaxis


```C++
POSITION AddTailI(
   void *pObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pObj* 
</dt> <dd>

Puntero al elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor POSITION para la nueva posición de cola.

## <a name="remarks"></a>Observaciones

Si se produce un error en el método, devuelve **NULL**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




