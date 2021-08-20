---
title: Método IMediaRenderer IsVideoSupported
description: Recupera un valor que indica si la DMR es capaz de reproducir contenido de vídeo.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- Método IsVideoSupported de Media Streaming API
- Método IsVideoSupported de Media Streaming API, interfaz IMediaRenderer
- IMediaRenderer interface Media Streaming API , Método IsVideoSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c1f6fa149c6c5025d3fd2c785dc2f4a8451fabed3906b559674d8038662c21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972314"
---
# <a name="imediarendererisvideosupported-method"></a>IMediaRenderer::IsVideoSupported (método)

Recupera un valor que indica si la DMR es capaz de reproducir contenido de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Valor booleano que es **True si** la DMR es capaz de reproducir contenido de vídeo y **False** si no lo es.

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

 

 





