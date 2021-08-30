---
description: El método AddTail anexa una lista al final de la lista.
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: 'Método CGenericList.AddTail (Wxlist.h): parámetro pList'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1cf647fb70b6d2896991bda2e8558ad34407f3427a2eef2d2ce8cd4295c95486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814005"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a>Método CGenericList.AddTail (Wxlist.h): parámetro pList

El `AddTail` método anexa una lista al final de la lista.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Plist* 
</dt> <dd>

Puntero a la lista que se anexará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist.h (incluir Secuencias.h) |
| Biblioteca| Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CGenericList (Clase)**](cgenericlist.md)
</dt> </dl>

 

 




