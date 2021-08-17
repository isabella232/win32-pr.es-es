---
description: El método SourceThreadCanWait contiene o libera el subproceso de streaming.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Método CBaseRenderer.SourceThreadCanWait (Renbase.h)
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
ms.openlocfilehash: 6ba9f8e202d7c98bfea5d7068fa63a8d889d88fb10b4c6a7cb3516fadbca7ebd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954774"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a>Método CBaseRenderer.SourceThreadCanWait

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

Valor booleano que indica si se debe contener el subproceso de streaming. Si **es TRUE,** el subproceso de streaming se bloquea mientras el filtro espera a representar los ejemplos siguientes. Si **es FALSE**, se libera el subproceso de streaming.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Llamar al método con el valor FALSE obliga al filtro a volver `SourceThreadCanWait` de una llamada [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) bloqueada.  Cuando el filtro se está ejecutando, bloquea las **llamadas receive** hasta el tiempo de presentación del ejemplo actual. Cuando el filtro está en pausa, bloquea las llamadas **receive** indefinidamente. Este comportamiento regula el flujo de datos en la secuencia. Sin embargo, cuando el filtro se detiene o se vacía, no debe bloquearse.

El bloqueo se controla mediante el método [**CBaseRenderer::WaitForRenderTime,**](cbaserenderer-waitforrendertime.md) que espera dos eventos: [**CBaseRenderer::m \_ RenderEvent**](cbaserenderer-m-renderevent.md) y [**CBaseRenderer::m \_ ThreadSignal.**](cbaserenderer-m-threadsignal.md) El **evento m \_ RenderEvent** se señala cuando llega el tiempo de presentación. El **evento \_ m ThreadSignal** se señala cuando `SourceThreadCanWait` se llama a con el valor **FALSE**. Al `SourceThreadCanWait` llamar a con el valor **TRUE** se restablece el evento.

Los [**métodos CBaseRenderer::Stop**](cbaserenderer-stop.md) y [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) llaman con el valor `SourceThreadCanWait` **FALSE** (liberando el subproceso de streaming). Los [**métodos CBaseRenderer::P ause**](cbaserenderer-pause.md), [**CBaseRenderer::Run**](cbaserenderer-run.md)y [**CBaseRenderer::EndFlush**](cbaserenderer-endflush.md) llaman `SourceThreadCanWait` con el valor **TRUE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




