---
title: Método IBasicDevice FriendlyName
description: Recupera el nombre descriptivo del dispositivo.
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- Método FriendlyName de Media Streaming API
- Media Streaming API del método FriendlyName, interfaz IBasicDevice
- IBasicDevice interface Media Streaming API , FriendlyName (método)
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35084fafb92b3716208aa6062f065cc4e25a45d2d1a412083076b9e355d2ce43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735619"
---
# <a name="ibasicdevicefriendlyname-method"></a>IBasicDevice::FriendlyName (método)

Recupera el nombre descriptivo del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe un puntero al nombre descriptivo del dispositivo.

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

 

 





