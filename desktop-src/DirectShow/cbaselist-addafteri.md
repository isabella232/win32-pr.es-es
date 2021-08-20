---
description: El método AddAfterI inserta un elemento después de la posición especificada.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Método CBaseList.AddAfterI (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b72be7342e6085b773ef2493f5ad138f73349dffcdafc1a60a380692df3f16ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016993"
---
# <a name="cbaselistaddafteri-method"></a>Método CBaseList.AddAfterI

El `AddAfterI` método inserta un elemento después de la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Posición después de la cual se va a agregar el elemento.

</dd> <dt>

*pObj* 
</dt> <dd>

Puntero al elemento que se agregará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el indicador de posición del elemento insertado.

## <a name="remarks"></a>Comentarios

Si *pos* es **NULL,** este método agrega el elemento al final de la lista (equivalente a llamar al método [**CBaseList::AddHeadI).**](cbaselist-addheadi.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 




