---
description: Obtenga información sobre el método de constructor para CGenericList. CGenericList (Wxlist. h). Este método usa el parámetro ' pName '.
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: 'Constructor CGenericList. CGenericList (Wxlist. h): parámetro pName'
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
ms.openlocfilehash: 4a2aa2347e963839c18d904f2819d50de8d6d9c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "103914834"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a>Constructor CGenericList. CGenericList (Wxlist. h): parámetro pName

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero al nombre de la lista.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Por motivos de eficacia, la `CGenericList` clase mantiene una memoria caché de nodos de lista. Esta versión del constructor utiliza un tamaño de caché predeterminado.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist. h (incluir streams. h) |
| Biblioteca| Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




