---
description: El método AddAfter inserta una lista después de la posición especificada y usa los parámetros ' pos ' y ' plist '.
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: 'Método CGenericList. AddAfter (Wxlist. h): parámetros de pos y plist'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6bbe26e98acc999f067a7b0e96c3716e7e0c0c0
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104548166"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a>Método CGenericList. AddAfter (Wxlist. h): parámetros de pos y plist

El `AddAfter` método inserta una lista después de la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Posición en la que se va a insertar la lista. La lista se inserta después de esta posición.

</dd> <dt>

*pList* 
</dt> <dd>

Puntero a la lista que se va a insertar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist. h (incluir streams. h) |
| Biblioteca| Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




