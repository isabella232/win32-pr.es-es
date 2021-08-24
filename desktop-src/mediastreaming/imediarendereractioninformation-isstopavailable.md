---
title: Método IMediaRendererActionInformation IsStopAvailable
description: Recupera un valor que indica si la DMR está aceptando actualmente el método StopAsync.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- Media Streaming API del método IsStopAvailable
- Método IsStopAvailable de Media Streaming API, interfaz IMediaRendererActionInformation
- IMediaRendererActionInformation interface Media Streaming API , IsStopAvailable method
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c177c46c62309525d9362f985075cec293105a80678b3b857eafa0524179d17e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712895"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a>IMediaRendererActionInformation::IsStopAvailable (método)

Recupera un valor que indica si la DMR acepta actualmente el [**método StopAsync.**](imediarenderer-stopasync.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Valor booleano que es **True si** la DMR acepta actualmente el método [**StopAsync**](imediarenderer-stopasync.md) y **False** si no lo está.

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

 

