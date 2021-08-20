---
title: Método IDeviceIcon Stream
description: Recupera el icono como una secuencia.
ms.assetid: 0B9E852F-4F72-4721-8F88-24A850A088C4
keywords:
- Stream method Media Streaming API
- Stream method Media Streaming API , IDeviceIcon interface
- IDeviceIcon interface Media Streaming API , Método Stream
topic_type:
- apiref
api_name:
- IDeviceIcon.Stream
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75163836c2722156ec4bf6cd8b763a7c1b0f43b35a087c9dbdce6aef1ec99541
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871190"
---
# <a name="ideviceiconstream-method"></a>IDeviceIcon::Stream (Método)

Recupera el icono como una secuencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Stream(
  [out] IRandomAccessStreamWithContentType **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe una referencia a [**un IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) que se puede usar para recuperar los datos de la imagen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

