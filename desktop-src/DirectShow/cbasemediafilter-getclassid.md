---
description: 'El método GetClassID recupera el identificador de clase. Este método implementa el método IPersist:: GetClassID.'
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: Método CBaseMediaFilter. GetClassID (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dafacba684711c5c04a155d2609e0bc68450fa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660254"
---
# <a name="cbasemediafiltergetclassid-method"></a>CBaseMediaFilter. GetClassID (método)

El `GetClassID` método recupera el identificador de clase. Este método implementa el método **IPersist:: GetClassID** .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pClsID* 
</dt> <dd>

Puntero a una variable que recibe el identificador de clase.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el \_ puntero S o E \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




