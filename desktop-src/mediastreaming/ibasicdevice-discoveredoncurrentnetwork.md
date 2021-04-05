---
title: IBasicDevice DiscoveredOnCurrentNetwork, método
description: Recupera un valor que indica si el dispositivo está en la red actual.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- Método DiscoveredOnCurrentNetwork API de streaming de multimedia
- Método DiscoveredOnCurrentNetwork API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método DiscoveredOnCurrentNetwork
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
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419440"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a>IBasicDevice::D método iscoveredOnCurrentNetwork

Recupera un valor que indica si el dispositivo está en la red actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Recibe un puntero a un valor booleano que es **true** si el dispositivo está en la red actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





