---
description: 'Método CBasePin.Inactive: el método Inactivo notifica al pin que el filtro ya no está activo.'
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Método CBasePin.Inactive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c0d9ec403b53c3197c001e966ce7efd5eb8bed2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973985"
---
# <a name="cbasepininactive-method"></a>Método CBasePin.Inactive

El `Inactive` método notifica al pin que el filtro ya no está activo.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Cuando se detiene el filtro, la [**clase CBaseFilter**](cbasefilter.md) llama a este método en todos los pines conectados del filtro.

Este método no hace nada en la clase base. Las clases derivadas deben invalidar este método para liberar los recursos obtenidos por el [**método CBasePin::Active;**](cbasepin-active.md) por ejemplo, para desasignar los asignadores del pin.

El estado interno del administrador de gráficos de filtro no se actualiza hasta después de que este método vuelva, por lo que no pruebe el estado de este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




