---
description: 'Método CPosPassThru.GetMediaTime: el método GetMediaTime recupera las marcas de tiempo en el ejemplo actual.'
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Método CPosPassThru.GetMediaTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 328a0ae09c80a687863cfedb994f5a80cebebf14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072266"
---
# <a name="cpospassthrugetmediatime-method"></a>Método CPosPassThru.GetMediaTime

El `GetMediaTime` método recupera las marcas de tiempo en el ejemplo actual.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStartTime* 
</dt> <dd>

Puntero a una variable que recibe la hora de inicio, en unidades del formato de hora actual.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntero a una variable que recibe la hora de finalización, en unidades del formato de hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ FAIL.

## <a name="remarks"></a>Observaciones

Invalide este método si el filtro almacena en caché las marcas de tiempo en los ejemplos que recibe.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 




