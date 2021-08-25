---
title: Método IBasicDevice IpAddresses
description: Devuelve un vector de direcciones IP.
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- Método IpAddresses de Media Streaming API
- Media Streaming API del método IpAddresses, interfaz IBasicDevice
- IBasicDevice interface Media Streaming API , método IpAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc997abb24c007e9e3e4d5c8028762daaca20e434ca4e3ab22fb278f567f998c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847685"
---
# <a name="ibasicdeviceipaddresses-method"></a>IBasicDevice::IpAddresses (método)

Devuelve un vector de direcciones IP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe una colección enumerable de punteros a direcciones IP.

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

 

 





