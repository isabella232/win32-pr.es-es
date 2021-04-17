---
description: El método Remove quita el elemento en la posición especificada.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: Método CGenericList. Remove (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5fc3d0cd76cd78c83fa210d8b91ba97b93b92f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660836"
---
# <a name="cgenericlistremove-method"></a>CGenericList. Remove (método)

El `Remove` método quita el elemento en la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
OBJECT* Remove(
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

Devuelve un puntero a un objeto de tipo **Object** (el tipo de plantilla).

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

[**Clase CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




