---
title: Método IMediaRendererActionInformation IsMuteAvailable
description: Recupera un valor que indica si la DMR es capaz de silenciar el audio.
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- Método IsMuteAvailable de Media Streaming API
- Media Streaming API del método IsMuteAvailable , interfaz IMediaRendererActionInformation
- IMediaRendererActionInformation interface Media Streaming API , método IsMuteAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 331e2831ff18656f23a3d7067b8ab472835bf4a25760f6e86a92302621048a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871072"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a>IMediaRendererActionInformation::IsMuteAvailable (Método)

Recupera un valor que indica si la DMR es capaz de silenciar el audio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Valor booleano que es **True si** la DMR es capaz de silenciar el audio y **False** si no lo es.

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

 

