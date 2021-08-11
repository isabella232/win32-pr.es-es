---
title: Método IBasicDevice PresentationUrl
description: Recupera la dirección URL de presentación del dispositivo.
ms.assetid: F1EF1BBE-F35D-4828-B4F6-D6DEFF5A6391
keywords:
- Método PresentationUrl de Media Streaming API
- Método PresentationUrl de Media Streaming API, interfaz IBasicDevice
- IBasicDevice interface Media Streaming API , Método PresentationUrl
topic_type:
- apiref
api_name:
- IBasicDevice.PresentationUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60d5908b80e7b413ca646279a751e12ec7d9c7e6e98ae7ecff3ad1f1d9e60bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235942"
---
# <a name="ibasicdevicepresentationurl-method"></a>IBasicDevice::P resentationUrl (método)

Recupera la dirección URL de presentación del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PresentationUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe un puntero a la dirección URL de presentación del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





