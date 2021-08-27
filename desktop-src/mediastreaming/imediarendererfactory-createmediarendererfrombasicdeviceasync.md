---
title: Método IMediaRendererFactory CreateMediaRendererFromBasicDeviceAsync
description: Crea de forma asincrónica una nueva instancia de un objeto que implementa la interfaz IMediaRenderer mediante la interfaz IBasicDevice especificada.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- Método CreateMediaRendererFromBasicDeviceAsync de Media Streaming API
- Método Media Streaming API de CreateMediaRendererFromBasicDeviceAsync, interfaz IMediaRendererFactory
- Interfaz IMediaRendererFactory Media Streaming API, método CreateMediaRendererFromBasicDeviceAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b9ee80a4f681bb57d62f84d35cf3a254e38982a10f642a35e35187f6af9e48e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092295"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a>IMediaRendererFactory::CreateMediaRendererFromBasicDeviceAsync (método)

Crea de forma asincrónica una nueva instancia de un objeto que implementa la [**interfaz IMediaRenderer**](imediarenderer.md) mediante la interfaz [**IBasicDevice**](ibasicdevice.md) especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*basicDevice* \[ En\]
</dt> <dd>

Puntero a una [**interfaz IBasicDevice**](ibasicdevice.md) que representa el dispositivo para el que se creará una instancia de [**IMediaRenderer.**](imediarenderer.md)

</dd> <dt>

*value* \[ out, retval\]
</dt> <dd>

Recibe una referencia a un [**objeto CreateMediaRendererOperation**](createmediarendereroperation.md) que se usa para obtener los resultados de la operación asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

