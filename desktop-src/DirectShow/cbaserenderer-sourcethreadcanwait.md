---
description: El método SourceThreadCanWait contiene o libera el subproceso de streaming.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Método CBaseRenderer. SourceThreadCanWait (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661269"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a>CBaseRenderer. SourceThreadCanWait, método

El `SourceThreadCanWait` método contiene o libera el subproceso de streaming.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bCanWait* 
</dt> <dd>

Valor booleano que indica si se va a contener el subproceso de streaming. Si es **true**, se bloquea el subproceso de streaming mientras el filtro espera a representar los ejemplos siguientes. Si es **false**, se libera el subproceso de streaming.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Al llamar al `SourceThreadCanWait` método con el valor **false** , el filtro se devuelve de una llamada a [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) bloqueada. Cuando el filtro se está ejecutando, bloquea las llamadas de **recepción** hasta el momento de la presentación del ejemplo actual. Cuando el filtro está en pausa, bloquea las llamadas de **recepción** indefinidamente. Este comportamiento regula el flujo de datos en la secuencia. Sin embargo, cuando el filtro se detiene o se vuelca, no debería bloquearse.

El bloqueo se controla mediante el método [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) , que espera dos eventos: [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) y [**CBaseRenderer:: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md). El evento **m \_ RenderEvent** se señala cuando llega el momento de la presentación. El evento **m \_ ThreadSignal** se señaliza cuando `SourceThreadCanWait` se llama a con el valor **false**. Al llamar a `SourceThreadCanWait` con el valor **true** , se restablece el evento.

Los métodos [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) y [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) llaman a `SourceThreadCanWait` con el valor **false** (liberando el subproceso de streaming). Los métodos [**CBaseRenderer::P ause**](cbaserenderer-pause.md), [**CBaseRenderer:: Run**](cbaserenderer-run.md)y [**CBaseRenderer:: EndFlush**](cbaserenderer-endflush.md) llaman a `SourceThreadCanWait` con el valor **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




