---
description: El método WaitForRenderTime espera el tiempo de presentación del ejemplo actual.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Método CBaseRenderer. WaitForRenderTime (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a537728ca0874fa1dfd69b4712bcc97cf23850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660134"
---
# <a name="cbaserendererwaitforrendertime-method"></a>CBaseRenderer. WaitForRenderTime, método

El `WaitForRenderTime` método espera el tiempo de presentación del ejemplo actual.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** .



| Código devuelto                                                                                           | Descripción                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>                                                       |
| <dl> <dt>**Estado de VFW \_ E \_ \_ cambiado**</dt> </dl> | El estado del filtro cambió antes de que llegara el tiempo de presentación.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método espera hasta que se produce uno de los siguientes casos:

-   Llega el tiempo de presentación del ejemplo, en el que se puede representar el ejemplo.
-   El filtro detiene o inicia el vaciado de datos.

Si llega el momento de la presentación, se señala el evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) . Si el estado cambia, se señala el evento [**CBaseRenderer:: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md) . Este método espera en ambos eventos. La clase derivada puede invalidar este método para esperar en eventos adicionales, si es necesario.

Este método llama al método [**CBaseRenderer:: OnWaitStart**](cbaserenderer-onwaitstart.md) cuando comienza la espera y el método [**CBaseRenderer:: OnWaitEnd**](cbaserenderer-onwaitend.md) cuando se realiza la espera. Ninguno de los métodos realiza ninguna acción en la clase base, pero la clase derivada puede invalidarlos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




