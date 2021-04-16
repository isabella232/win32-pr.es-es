---
description: El método DoBufferProcessingLoop genera datos multimedia y los entrega al pin de entrada de nivel inferior.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: CSourceStream. DoBufferProcessingLoop (método) (Source. h)
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
ms.openlocfilehash: 809694cacf0c30acf88ddf7d14c7f5ea1f654436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690547"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a>CSourceStream. DoBufferProcessingLoop, método

El `DoBufferProcessingLoop` método genera datos multimedia y los entrega al pin de entrada de nivel inferior.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | El subproceso ha recibido una solicitud de detención.<br/>                              |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | La secuencia finalizó o el filtro descendente no acepta ejemplos.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método implementa el bucle principal que procesa los datos y los entrega hacia abajo. Cada vez a través del bucle, el método recupera un ejemplo de medio vacío del asignador. Pasa el ejemplo al método [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) . El método **FillBuffer** , que la clase derivada debe implementar, genera datos multimedia y los coloca en el búfer de ejemplo.

El bucle finaliza cuando se produce cualquiera de las siguientes situaciones:

-   El método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del PIN de entrada rechaza un ejemplo.
-   El método **FillBuffer** devuelve S \_ false, que indica el final de la secuencia o devuelve un código de error.
-   El subproceso recibe una solicitud [**CSourceStream:: Stop**](csourcestream-stop.md) .

El `DoBufferProcessingLoop` método controla la notificación de final de secuencia. Si se produce un error, envía un [**evento \_ ERRORABORT de EC**](ec-errorabort.md) al administrador de gráficos de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




