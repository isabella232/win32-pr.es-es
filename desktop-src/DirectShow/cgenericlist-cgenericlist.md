---
description: Obtenga información sobre el método de constructor para CGenericList. CGenericList (Wxlist. h). Este método usa los parámetros ' pName ' y ' iItems '.
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: Constructor CGenericList. CGenericList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77a3dd932872b9d96c754ac5b1db184dcf99cf03
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104362839"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a>Constructor CGenericList. CGenericList (Wxlist. h): parámetros pName, iItems

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CGenericList(
   TCHAR *pName,
   INT   iItems,
   BOOL  bLock,
   BOOL  bAlert
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero al nombre de la lista.

</dd> <dt>

*iItems* 
</dt> <dd>

Tamaño de la memoria caché de nodo.

</dd> <dt>

*Sin* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*bAlert* 
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Por motivos de eficacia, la `CGenericList` clase mantiene una memoria caché de nodos de lista. Si conoce aproximadamente el número de elementos que contendrá la lista, use esta versión del constructor.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist. h (incluir streams. h) |
| Biblioteca| Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




