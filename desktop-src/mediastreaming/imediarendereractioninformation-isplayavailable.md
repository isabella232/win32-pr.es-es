---
title: Método IMediaRendererActionInformation IsPlayAvailable
description: Recupera un valor que indica si la DMR acepta actualmente los métodos PlayAsync y PlayAtSpeedAsync.
ms.assetid: 969C55FA-872D-4063-B85C-573C8DA5593C
keywords:
- Método IsPlayAvailable de Media Streaming API
- Método IsPlayAvailable de Media Streaming API, interfaz IMediaRendererActionInformation
- IMediaRendererActionInformation interface Media Streaming API , IsPlayAvailable method
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPlayAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 912e5478ef1d9bd7114d198a9671d38ba7b721c9dbd82d2a8080b5a7876e76cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235850"
---
# <a name="imediarendereractioninformationisplayavailable-method"></a>IMediaRendererActionInformation::IsPlayAvailable (Método)

Recupera un valor que indica si la DMR acepta actualmente los métodos [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) y [**PlayAtSpeedAsync.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsPlayAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Valor booleano que es **True si** la DMR acepta actualmente los métodos [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) y [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) y **False** si no lo está.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

