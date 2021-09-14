---
description: El método WaitForRenderTime espera el tiempo de presentación del ejemplo actual.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Método CBaseRenderer.WaitForRenderTime (Renbase.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061742"
---
# <a name="cbaserendererwaitforrendertime-method"></a>Método CBaseRenderer.WaitForRenderTime

El `WaitForRenderTime` método espera el tiempo de presentación del ejemplo actual.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT.**



| Código devuelto                                                                                           | Descripción                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                                                       |
| <dl> <dt>**CAMBIO DEL \_ ESTADO DE VFW E \_ \_**</dt> </dl> | El estado del filtro cambió antes de que llegara el tiempo de presentación.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método espera hasta que se produzca una de las siguientes acciones:

-   Llega el tiempo de presentación de la muestra, momento en el que se puede representar la muestra.
-   El filtro se detiene o comienza a vaciar los datos.

Si llega el tiempo de presentación, se señala el evento [**\_ RenderEvent CBaseRenderer::m.**](cbaserenderer-m-renderevent.md) Si cambia el estado, se señala el evento [**\_ ThreadSignal CBaseRenderer::m.**](cbaserenderer-m-threadsignal.md) Este método espera en ambos eventos. La clase derivada puede invalidar este método para esperar eventos adicionales, si es necesario.

Este método llama al [**método CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) cuando comienza la espera y al método [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) cuando se realiza la espera. Ninguno de los métodos hace nada en la clase base, pero la clase derivada puede invalidarlos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




