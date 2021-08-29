---
description: 'Método CPosPassThru.GetMediaTime: el método GetMediaTime recupera las marcas de tiempo del ejemplo actual.'
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
ms.openlocfilehash: ec2767f3a20b6acc162da8670eefcd6d399639d5acf713b6dc54caf56f6edabe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084175"
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

## <a name="remarks"></a>Comentarios

Invalide este método si el filtro almacena en caché las marcas de tiempo en los ejemplos que recibe.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 




