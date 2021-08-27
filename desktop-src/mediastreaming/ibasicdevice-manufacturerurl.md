---
title: Método IBasicDevice ManufacturerUrl
description: Recupera la dirección URL del fabricante del dispositivo.
ms.assetid: E8372D15-D8B5-49E4-950A-96B4A88B0450
keywords:
- Método ManufacturerUrl de Media Streaming API
- Método ManufacturerUrl de Media Streaming API, interfaz IBasicDevice
- IBasicDevice interface Media Streaming API , método ManufacturerUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 306b4c194d7354b071d4daaf223a17f977b38b44243adaef856f9acffbf49c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972344"
---
# <a name="ibasicdevicemanufacturerurl-method"></a>IBasicDevice::ManufacturerUrl (método)

Recupera la dirección URL del fabricante del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ManufacturerUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe un puntero a la dirección URL del fabricante del dispositivo.

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

 

 





