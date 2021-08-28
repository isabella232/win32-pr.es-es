---
description: El método Invoke proporciona acceso a métodos y propiedades expuestos por un objeto .
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: Método CDeferredCommand.Invoke (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1df087e71ba03ef67ea250235a4ef8a9ef5e6623efe67594381111de6088cf7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074379"
---
# <a name="cdeferredcommandinvoke-method"></a>Método CDeferredCommand.Invoke

El `Invoke` método proporciona acceso a métodos y propiedades expuestos por un objeto .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Invoke();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve VFW \_ E \_ ALREADY \_ CANCELLED si m **\_ pQueue** es **NULL.** De lo contrario, devuelve **el valor HRESULT** resultante de una llamada a **IDispatch::GetTypeInfo** o **IUnknown::QueryInterface**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDeferredCommand (clase)**](cdeferredcommand.md)
</dt> </dl>

 

 




