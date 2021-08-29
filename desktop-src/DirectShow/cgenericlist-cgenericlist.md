---
description: Obtenga información sobre el método de constructor para CGenericList.CGenericList (Wxlist.h). Este método usa los parámetros "pName" e "iItems".
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: Constructor CGenericList.CGenericList (Wxlist.h)
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
ms.openlocfilehash: 0885ecc91b35e9845703b7169f45fd6f7aa3d55aa10f57fc7ddc68ef7d42129e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813995"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a>Constructor CGenericList.CGenericList (Wxlist.h): pName, parámetros iItems

Método constructor.

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

Tamaño de la caché del nodo.

</dd> <dt>

*Bloquear* 
</dt> <dd>

No se usa.

</dd> <dt>

*bAlert* 
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para mejorar la eficacia, `CGenericList` la clase mantiene una caché de nodos de lista. Si sabe aproximadamente cuántos elementos contendrán la lista, use esta versión del constructor.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist.h (incluir Secuencias.h) |
| Biblioteca| Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CGenericList (clase)**](cgenericlist.md)
</dt> </dl>

 

 




