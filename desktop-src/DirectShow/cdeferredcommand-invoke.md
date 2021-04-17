---
description: El método Invoke proporciona acceso a los métodos y propiedades expuestos por un objeto.
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: Método CDeferredCommand. Invoke (Ctlutil. h)
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
ms.openlocfilehash: 268cfc3d4665eeacafbd695b974f55445747e151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680500"
---
# <a name="cdeferredcommandinvoke-method"></a>CDeferredCommand. Invoke (método)

El `Invoke` método proporciona acceso a los métodos y propiedades expuestos por un objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Invoke();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve VFW \_ E \_ ya \_ cancelado si **m \_ pQueue** es **null**. De lo contrario, devuelve el **valor HRESULT** resultante de una llamada a **IDispatch:: GetTypeInfo** o **IUnknown:: QueryInterface**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




