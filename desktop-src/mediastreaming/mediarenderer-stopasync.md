---
title: Método MediaRenderer.StopAsync
description: Indica a la DMR de forma asincrónica que deje de reproducir el contenido actual. | Método MediaRenderer.StopAsync
ms.assetid: 04cf6d5a-8aa5-4821-8117-f250bfaf7ebd
keywords:
- Método StopAsync de Media Streaming API
- Método StopAsync de Media Streaming API, interfaz de MediaRenderer
- MediaRenderer interface Media Streaming API , método StopAsync
topic_type:
- apiref
api_name:
- MediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c13e69952261643f2ac74df1e3978fb10e846488ee2c4794ee3ecac17251469
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972144"
---
# <a name="mediarendererstopasync-method"></a>Método MediaRenderer.StopAsync

Indica a la DMR de forma asincrónica que deje de reproducir el contenido actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT StopAsync(
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

 

 





