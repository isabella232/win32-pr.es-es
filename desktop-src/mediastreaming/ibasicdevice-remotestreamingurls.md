---
title: Método IBasicDevice RemoteStreamingUrls
description: Devuelve un vector de direcciones URL de streaming remoto.
ms.assetid: 19B4475F-A7E4-4DC4-9C88-68D91D023AF4
keywords:
- Método RemoteStreamingUrls de Media Streaming API
- Método RemoteStreamingUrls de Media Streaming API, interfaz IBasicDevice
- IBasicDevice interface Media Streaming API , método RemoteStreamingUrls
topic_type:
- apiref
api_name:
- IBasicDevice.RemoteStreamingUrls
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90d98d908cb582c0c2885a9b24a0a525f1e719c82bdffe20e74597ca5fc262a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972334"
---
# <a name="ibasicdeviceremotestreamingurls-method"></a>IBasicDevice::RemoteStreamingUrls (método)

Devuelve un vector de direcciones URL de streaming remoto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoteStreamingUrls(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe una colección enumerable de punteros a direcciones URL de streaming remoto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





