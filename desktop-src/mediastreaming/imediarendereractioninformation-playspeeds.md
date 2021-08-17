---
title: Método IMediaRendererActionInformation PlaySpeeds
description: Recupera la lista completa de valores de PlaySpeed aceptados por la DMR.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- Método PlaySpeeds de Media Streaming API
- Método PlaySpeeds Media Streaming API, interfaz IMediaRendererActionInformation
- IMediaRendererActionInformation interface Media Streaming API , método PlaySpeeds
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 573fe9da4e71f9c16a9850da352e866ddbb0f77abc8c30861f2aa29647065fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972204"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a>IMediaRendererActionInformation::P laySpeeds (método)

Recupera la lista completa de valores [**de PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) aceptados por la DMR.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe un vector de [**estructuras PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) que especifica la lista completa de valores **playSpeed** aceptados por la DMR.

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

 

