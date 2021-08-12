---
title: Método ActionInformation de ITransportParameters
description: Obtiene una interfaz IMediaRendererActionInformation que proporciona información sobre qué métodos se pueden invocar actualmente en la DMR.
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- Método ActionInformation de Media Streaming API
- Método ActionInformation de Media Streaming API, interfaz ITransportParameters
- ITransportParameters interface Media Streaming API , método ActionInformation
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 551612fcaffb9379823efea15f29ed9feba1ff3d0c5af6e7271b61ad9d6036f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235860"
---
# <a name="itransportparametersactioninformation-method"></a>ITransportParameters::ActionInformation (método)

Obtiene una interfaz [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) que proporciona información sobre qué métodos se pueden invocar actualmente en la DMR.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out, retval\]
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

[**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

