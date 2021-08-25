---
description: Obtenga información sobre el método de constructor para CGenericList.CGenericList (Wxlist.h). Este método usa el parámetro 'pName'.
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: 'Constructor CGenericList.CGenericList (Wxlist.h): parámetro pName'
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
ms.openlocfilehash: 117138e80db91529d6a2baf93577a6a4dfd542d2975bf2ce6f89124a3d7aefe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813845"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a>Constructor CGenericList.CGenericList (Wxlist.h): parámetro pName

Método constructor.

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

## <a name="remarks"></a>Comentarios

Para mejorar la eficacia, `CGenericList` la clase mantiene una caché de nodos de lista. Esta versión del constructor usa un tamaño de caché predeterminado.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Wxlist.h (incluir Secuencias.h) |
| Biblioteca| Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CGenericList (clase)**](cgenericlist.md)
</dt> </dl>

 

 




