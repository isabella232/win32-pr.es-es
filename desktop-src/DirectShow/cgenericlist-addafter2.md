---
description: El método AddAfter inserta una lista después de la posición especificada y usa los parámetros "pos" y "plist".
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: 'Método CGenericList.AddAfter (Wxlist.h): pos, parámetros plist'
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
ms.openlocfilehash: 846e37b961af8d2492b3aff032193e87fb3603eb1751c25f0e3ca8e0c5d38618
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697485"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a>Método CGenericList.AddAfter (Wxlist.h): pos, parámetros plist

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

Posición para insertar la lista. La lista se inserta después de esta posición.

</dd> <dt>

*Plist* 
</dt> <dd>

Puntero a la lista que se insertará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist.h (incluir Secuencias.h) |
| Biblioteca| Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CGenericList (clase)**](cgenericlist.md)
</dt> </dl>

 

 




