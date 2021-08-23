---
title: Método IBasicDevice UniqueDeviceName
description: Recupera el nombre de dispositivo único (UDN) del dispositivo.
ms.assetid: 393EFF96-69E1-4081-905D-D8CC47B5FC4A
keywords:
- Método UniqueDeviceName de Media Streaming API
- Método UniqueDeviceName de Media Streaming API, interfaz IBasicDevice
- IBasicDevice interface Media Streaming API , UniqueDeviceName (método)
topic_type:
- apiref
api_name:
- IBasicDevice.UniqueDeviceName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b70fbc2021cf717cdb49d8a222aa33ad4e9213f297364b81af065c3bbeaed99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972324"
---
# <a name="ibasicdeviceuniquedevicename-method"></a>IBasicDevice::UniqueDeviceName (método)

Recupera el nombre de dispositivo único (UDN) del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UniqueDeviceName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe un puntero al UDN del modelo del dispositivo.

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

 

 





