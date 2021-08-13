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
ms.openlocfilehash: 605962315e4eab2cdbd5beab264747d282d78ef7c6f44b3bbcbf2f249bac7548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473498"
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



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





