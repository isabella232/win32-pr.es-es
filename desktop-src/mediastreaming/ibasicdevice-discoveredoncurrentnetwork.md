---
title: Método IBasicDevice DiscoveredOnCurrentNetwork
description: Recupera un valor que indica si el dispositivo está en la red actual.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- Método DiscoveredOnCurrentNetwork de Media Streaming API
- Método DiscoveredOnCurrentNetwork de Media Streaming API, interfaz IBasicDevice
- IBasicDevice interface Media Streaming API , método DiscoveredOnCurrentNetwork
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e79a012413b3b3d78a9c4617f01ca6cc01cf7e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248498"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a>Método IBasicDevice::D iscoveredOnCurrentNetwork

Recupera un valor que indica si el dispositivo está en la red actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe un puntero a un valor booleano que es **True** si el dispositivo está en la red actual.

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

 

 





