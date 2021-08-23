---
title: Método IsAudioSupported de IMediaRenderer
description: Recupera un valor que indica si la DMR es capaz de reproducir contenido de audio.
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- Método IsAudioSupported de Media Streaming API
- Método IsAudioSupported de Media Streaming API, interfaz IMediaRenderer
- IMediaRenderer interface Media Streaming API , Método IsAudioSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5abe42e65e451464a5f7f3a4d59679db62c3634e95e89e5e275919dd0ece869e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777015"
---
# <a name="imediarendererisaudiosupported-method"></a>IMediaRenderer::IsAudioSupported (método)

Recupera un valor que indica si la DMR es capaz de reproducir contenido de audio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Valor booleano que es **True si** la DMR es capaz de reproducir contenido de audio y **False** si no lo es.

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

 

 





