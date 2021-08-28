---
title: Método PauseAsync de IMediaRenderer
description: Indica a la DMR de forma asincrónica que pause la reproducción del contenido actual. | Método PauseAsync de IMediaRenderer
ms.assetid: 2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B
keywords:
- Método PauseAsync de Media Streaming API
- Método PauseAsync de Media Streaming API, interfaz IMediaRenderer
- IMediaRenderer interface Media Streaming API , método PauseAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a953d024ee0f90f7cb466574b29d7e3cfe150072bf1a3787734f8365916cb2a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972274"
---
# <a name="imediarendererpauseasync-method"></a>IMediaRenderer::P auseAsync (método)

Indica a la DMR de forma asincrónica que pause la reproducción del contenido actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe una referencia a un [**objeto PlaybackOperation**](playbackoperation.md) que se usa para obtener los resultados de la operación asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





