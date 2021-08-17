---
title: Método IMediaRendererActionInformation IsPauseAvailable
description: Recupera un valor que indica si la DMR está aceptando actualmente el método PauseAsync.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- Método IsPauseAvailable de Media Streaming API
- Método IsPauseAvailable de Media Streaming API, interfaz IMediaRendererActionInformation
- IMediaRendererActionInformation interface Media Streaming API , método IsPauseAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fad69863306a8a937771f16c2ab9a83a2622c571d2cd5ee5658a279bf7564132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870852"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a>IMediaRendererActionInformation::IsPauseAvailable (método)

Recupera un valor que indica si la DMR está aceptando actualmente el [**método PauseAsync.**](imediarenderer-pauseasync.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Valor booleano que es **True si** la DMR acepta actualmente el método [**PauseAsync**](imediarenderer-pauseasync.md) y **False** si no lo está.

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

 

