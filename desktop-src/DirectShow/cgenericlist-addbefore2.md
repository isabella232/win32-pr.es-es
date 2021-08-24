---
description: El método AddBefore inserta una lista antes de la posición especificada. Este método usa los parámetros "pos" y "pList".
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: 'Método CGenericList.AddBefore (Wxlist.h): pos, parámetros pList'
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
ms.openlocfilehash: 6f05d67477bb7e6c89eddfe0a68ad47d83760762fc68cddf6f73c731886f88d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697455"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a>Método CGenericList.AddBefore (Wxlist.h): pos, parámetros pList

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

Posición para insertar la lista. La lista se inserta antes de esta posición.

</dd> <dt>

*Plist* 
</dt> <dd>

Puntero a la lista que se insertará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente. De lo contrario, **devuelve FALSE**.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist.h (incluir Secuencias.h) |
| Biblioteca| Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CGenericList (Clase)**](cgenericlist.md)
</dt> </dl>

 

 




