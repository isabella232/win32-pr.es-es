---
title: Método MediaRenderer.PauseAsync
description: Indica a la DMR de forma asincrónica que pause la reproducción del contenido actual. | Método MediaRenderer.PauseAsync
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- Método PauseAsync de Media Streaming API
- Método PauseAsync de Media Streaming API, interfaz de MediaRenderer
- MediaRenderer interface Media Streaming API , método PauseAsync
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbbc55931c7cc7fc5e2e5ec39ba63fe7a064478
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570605"
---
# <a name="mediarendererpauseasync-method"></a>Método MediaRenderer.PauseAsync

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

[**Representador de medios**](mediarenderer.md)
</dt> </dl>

 

 





