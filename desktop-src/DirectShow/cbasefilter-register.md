---
description: El método Register agrega el filtro al Registro.
ms.assetid: 934e421a-25a6-40fa-a48b-6d7331f34b78
title: Método CBaseFilter.Register (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Register
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 168d84d3bfc90fb710ae65a3b887eeb5575db407361a256c48161f0f7968a53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403528"
---
# <a name="cbasefilterregister-method"></a>Método CBaseFilter.Register

El `Register` método agrega el filtro al Registro.

> [!Note]  
> Este método está obsoleto. Se deben registrar nuevos filtros mediante la [**función AMovieDllRegisterServer2.**](amoviedllregisterserver2.md) Para obtener más información, [vea How to Register DirectShow Filters](how-to-register-directshow-filters.md).

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Register();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                          |
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                                  |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | No hay información de registro disponible.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




