---
description: El método GetClassID recupera el identificador de clase (CLSID) del objeto . Este método implementa el método IPersist::GetClassID.
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Método CSystemClock.GetClassID (Sysclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2f83d3e3c2efcbcb5d4604bc5c50a37dc020f0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070014"
---
# <a name="csystemclockgetclassid-method"></a>Método CSystemClock.GetClassID

El `GetClassID` método recupera el identificador de clase (CLSID) del objeto . Este método implementa el **método IPersist::GetClassID.**

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

Puntero a una variable que recibe el valor CLSID \_ SystemClock.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ POINTER.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | CSystemClock (clase)<br/>                                                                                                                                                              |
| Encabezado<br/>  | <dl> <dt>Sysclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




