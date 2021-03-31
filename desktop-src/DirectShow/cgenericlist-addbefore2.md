---
description: El método AddBefore inserta una lista antes de la posición especificada. Este método usa los parámetros ' pos ' y ' plist '.
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: 'Método CGenericList. AddBefore (Wxlist. h): parámetros de pos y plist'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6aa6aa71b1738a815beee9cdc7c0f47118eb27f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821586"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a>Método CGenericList. AddBefore (Wxlist. h): parámetros de pos y plist

El `AddBefore` método inserta una lista antes de la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Posición en la que se va a insertar la lista. La lista se inserta antes de esta posición.

</dd> <dt>

*pList* 
</dt> <dd>

Puntero a la lista que se va a insertar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true si es** correcto. De lo contrario, devuelve **false**.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist. h (incluir streams. h) |
| Biblioteca| Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




