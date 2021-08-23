---
description: El método Unregister quita el filtro del Registro.
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: Método CBaseFilter.Unregister (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Unregister
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c57d08c77c9c420cdc45b158a19fa610231f53f6b409d8b650953de0de8381a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317905"
---
# <a name="cbasefilterunregister-method"></a>CBaseFilter.Unregister (método)

El `Unregister` método quita el filtro del Registro.

> [!Note]  
> Este método está obsoleto. Los nuevos filtros deben anularse del registro mediante [**la función AMovieDllRegisterServer2.**](amoviedllregisterserver2.md) Para obtener más información, [vea How to Register DirectShow Filters](how-to-register-directshow-filters.md).

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Unregister();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




