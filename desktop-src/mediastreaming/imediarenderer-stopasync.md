---
title: Método IMediaRenderer StopAsync
description: Indica a la DMR de forma asincrónica que deje de reproducir el contenido actual. | Método IMediaRenderer StopAsync
ms.assetid: B6B0F3F2-E95E-4A58-9CBD-CF4CB24FDAD0
keywords:
- Método StopAsync de Media Streaming API
- Método StopAsync Media Streaming API, interfaz IMediaRenderer
- Interfaz IMediaRenderer Media Streaming API, método StopAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5f73d534fdd786038a242614a981f4915d92c13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363519"
---
# <a name="imediarendererstopasync-method"></a>IMediaRenderer::StopAsync (método)

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



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





