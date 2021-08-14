---
title: Método ActionInformation de IMediaRenderer
description: Recupera información sobre qué métodos se pueden invocar actualmente en la DMR.
ms.assetid: 7681FF92-DD13-4BBC-B860-E2BDFDA74FB9
keywords:
- Método ActionInformation de Media Streaming API
- Método ActionInformation de Media Streaming API, interfaz IMediaRenderer
- IMediaRenderer interface Media Streaming API , método ActionInformation
topic_type:
- apiref
api_name:
- IMediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3caf251c080f218b99861d4a81920cd5c95c1f0e53bc6b006c84536f33f7f29c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735528"
---
# <a name="imediarendereractioninformation-method"></a>IMediaRenderer::ActionInformation (método)

Recupera información sobre qué métodos se pueden invocar actualmente en la DMR.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe una referencia a una [**interfaz IMediaRendererActionInformation.**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)

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

 

