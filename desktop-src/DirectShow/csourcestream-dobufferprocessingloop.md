---
description: El método DoBufferProcessingLoop genera datos multimedia y los entrega al pin de entrada de bajada.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: Método CSourceStream.DoBufferProcessingLoop (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d23df592abd125fd64362af89b6f81c5e9dcc20f0aa6cc998974a8fd2d4d87f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953744"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a>Método CSourceStream.DoBufferProcessingLoop

El método genera datos multimedia y los entrega al `DoBufferProcessingLoop` pin de entrada de bajada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El subproceso recibió una solicitud de detenerse.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>    | El flujo finalizó o el filtro de nivel inferior no acepta ejemplos.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método implementa el bucle main que procesa los datos y los entrega de bajada. Cada vez que se recorre el bucle, el método recupera un ejemplo multimedia vacío del asignador. Pasa el ejemplo al método [**CSourceStream::FillBuffer.**](csourcestream-fillbuffer.md) El **método FillBuffer,** que la clase derivada debe implementar, genera datos multimedia y los coloca en el búfer de ejemplo.

El bucle finaliza cuando se produce alguna de las siguientes situaciones:

-   El método [**IMemInputPin::Receive del**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) pin de entrada rechaza un ejemplo.
-   El **método FillBuffer** devuelve S \_ FALSE, que indica el final de la secuencia, o devuelve un código de error.
-   El subproceso recibe una [**solicitud CSourceStream::Stop.**](csourcestream-stop.md)

El `DoBufferProcessingLoop` método controla la notificación de fin de flujo. Si se produce un error, envía un evento [**\_ EC ERRORABORT**](ec-errorabort.md) al administrador de gráficos de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




