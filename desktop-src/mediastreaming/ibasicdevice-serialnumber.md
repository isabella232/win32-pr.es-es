---
title: Método IBasicDevice SerialNumber
description: Recupera el número de serie del dispositivo.
ms.assetid: 238A5999-0E8B-4462-AFCF-790DB58CFCB4
keywords:
- Método SerialNumber de Media Streaming API
- Método SerialNumber de Media Streaming API, interfaz IBasicDevice
- IBasicDevice interface Media Streaming API , método SerialNumber
topic_type:
- apiref
api_name:
- IBasicDevice.SerialNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37a4985754982b8b64246d8d0d0fac0d2c37f4a37f159d2e5087497442c97a75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712945"
---
# <a name="ibasicdeviceserialnumber-method"></a>IBasicDevice::SerialNumber (Método)

Recupera el número de serie del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SerialNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe un puntero al número de serie del dispositivo.

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

 

 





