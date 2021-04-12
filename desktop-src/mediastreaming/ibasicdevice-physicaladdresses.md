---
title: IBasicDevice PhysicalAddresses, método
description: Devuelve un vector de direcciones físicas.
ms.assetid: 85F48EE3-14A1-46DA-A3C3-F94A8A43CF92
keywords:
- Método PhysicalAddresses API de streaming de multimedia
- Método PhysicalAddresses API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método PhysicalAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.PhysicalAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f1cd87435c78e1f6877d1bb6afd1b38981b05dc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358076"
---
# <a name="ibasicdevicephysicaladdresses-method"></a>IBasicDevice::P método hysicalAddresses

Devuelve un vector de direcciones físicas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PhysicalAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Recibe una colección enumerable de punteros a direcciones físicas.

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

 

 





