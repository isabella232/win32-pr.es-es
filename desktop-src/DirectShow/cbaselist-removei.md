---
description: El método removei quita el elemento en la posición especificada.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: Método CBaseList. removei (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671327"
---
# <a name="cbaselistremovei-method"></a>CBaseList. Remove (método)

El `RemoveI` método quita el elemento en la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Valor de posición que indica el elemento que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al elemento.

## <a name="remarks"></a>Observaciones

Este método elimina el nodo de la lista, pero no elimina el elemento contenido en ese nodo.

Si *pos* es **null**, el método devuelve **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseList**](cbaselist.md)
</dt> </dl>

 

 




