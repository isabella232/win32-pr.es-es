---
description: El método GetSetupData recupera los datos de registro del filtro.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Método CBaseFilter.GetSetupData (Amfilter.h)
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
ms.openlocfilehash: f86bc35688ab0ec1c19053a95cbfd2025cf45ad666ef419fdb8440c6a844cb61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640475"
---
# <a name="cbasefiltergetsetupdata-method"></a>Método CBaseFilter.GetSetupData

El `GetSetupData` método recupera los datos de registro del filtro.

> [!Note]  
> Este método está obsoleto. Lo llaman los métodos [**CBaseFilter::Register**](cbasefilter-register.md) y [**CBaseFilter::Unregister.**](cbasefilter-unregister.md)

 

## <a name="syntax"></a>Sintaxis


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a una [**estructura FILTER de AMOVIESETUP \_**](amoviesetup-filter.md) que contiene información de registro para el filtro.

## <a name="remarks"></a>Comentarios

La clase base devuelve **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




