---
description: El método get recupera el elemento en la posición especificada.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: Método CGenericList. get (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02af7d57d2219e6eb0506a8ab11521b4cf3570eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671144"
---
# <a name="cgenericlistget-method"></a>CGenericList. get (método)

El `Get` método recupera el elemento en la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Indicador de posición del elemento que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a un objeto de tipo **Object** (el tipo de plantilla).

## <a name="remarks"></a>Observaciones

Si *pos* es **null**, el método devuelve **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




