---
description: El método AddHead agrega una lista al frente de la lista.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: 'Método CGenericList.AddHead (Wxlist.h): parámetro pList'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c26667ce12af902f3d5cf355a6556dc95e5dd1f5e0cad77f944e663eeef8ce67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656160"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a>Método CGenericList.AddHead (Wxlist.h): parámetro pList

El `AddHead` método agrega una lista al frente de la lista.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Plist* 
</dt> <dd>

Puntero a la lista de elementos que se agregarán.

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

 

 




