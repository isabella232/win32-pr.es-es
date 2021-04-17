---
description: El método Find recupera la primera posición que contiene el elemento especificado.
ms.assetid: 8e2a3e5d-96e6-4f40-8e2a-4dc8c21088cd
title: Método CGenericList. Find (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Find
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a21f16e25d8a2ebba4494a850bc456a7b579f2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660844"
---
# <a name="cgenericlistfind-method"></a>CGenericList. Find (método)

El `Find` método recupera la primera posición que contiene el elemento especificado.

## <a name="syntax"></a>Sintaxis


```C++
POSITION Find(
   OBJECT *pObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pObj* 
</dt> <dd>

Puntero a un objeto de tipo **Object** (el tipo de plantilla).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de posición o **null** si el elemento no está en la lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




