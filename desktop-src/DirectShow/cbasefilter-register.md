---
description: El método Register agrega el filtro al registro.
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
ms.openlocfilehash: 1bd7ba5a57d670ef28ffda022c95c7dc5b12df77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361403"
---
# <a name="cbasefilterregister-method"></a>Método CBaseFilter.Register

El `Register` método agrega el filtro al registro.

> [!Note]  
> Este método está obsoleto. Los nuevos filtros deben registrarse mediante la [**función AMovieDllRegisterServer2.**](amoviedllregisterserver2.md) Para obtener más información, [vea How to Register DirectShow Filters](how-to-register-directshow-filters.md).

 

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

 

 




