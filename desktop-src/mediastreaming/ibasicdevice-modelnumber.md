---
title: Método IBasicDevice ModelNumber
description: Recupera el número de modelo del dispositivo.
ms.assetid: C4199135-0C6C-4427-8152-224D7D29C270
keywords:
- Método ModelNumber de Media Streaming API
- Método ModelNumber de Media Streaming API, interfaz IBasicDevice
- IBasicDevice interface Media Streaming API , método ModelNumber
topic_type:
- apiref
api_name:
- IBasicDevice.ModelNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2793a67e6dee60c20c613b32b96bb2dda76907b13bd5e7a9c71add86d2c35a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461905"
---
# <a name="ibasicdevicemodelnumber-method"></a>IBasicDevice::ModelNumber (Método)

Recupera el número de modelo del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ModelNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe un puntero al número de modelo del dispositivo.

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

 

 





