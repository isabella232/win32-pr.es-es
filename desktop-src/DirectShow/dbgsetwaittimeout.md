---
description: Establece el valor de tiempo de espera de depuración. Se omite en las compilaciones comerciales.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: Función DbgSetWaitTimeout (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5805112b19132045e0245ef7baf29cb5c844e290
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660404"
---
# <a name="dbgsetwaittimeout-function"></a>DbgSetWaitTimeout función)

Establece el valor de tiempo de espera de depuración. Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwTimeout* 
</dt> <dd>

Valor de tiempo de espera en milisegundos o infinito para esperar indefinidamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En las compilaciones de depuración, las funciones [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) y [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) usan este valor como el intervalo de tiempo de espera.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de depuración de espera](wait-debugging-functions.md)
</dt> </dl>

 

 




