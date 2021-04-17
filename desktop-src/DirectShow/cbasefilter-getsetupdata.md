---
description: El método GetSetupData recupera los datos de registro para el filtro.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Método CBaseFilter. GetSetupData (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40223a22f4de4a078ce84f8ebe49bddd5ab13575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661084"
---
# <a name="cbasefiltergetsetupdata-method"></a>CBaseFilter. GetSetupData, método

El `GetSetupData` método recupera los datos de registro para el filtro.

> [!Note]  
> Este método está obsoleto. Lo llaman los métodos [**CBaseFilter:: Register**](cbasefilter-register.md) y [**CBaseFilter:: unregister**](cbasefilter-unregister.md) .

 

## <a name="syntax"></a>Sintaxis


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a una estructura de [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) que contiene información de registro para el filtro.

## <a name="remarks"></a>Observaciones

La clase base devuelve **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




