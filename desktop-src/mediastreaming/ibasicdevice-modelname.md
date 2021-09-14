---
title: Método IBasicDevice ModelName
description: Recupera el nombre del modelo del dispositivo.
ms.assetid: 8F871E89-97C1-4788-83AB-B7E0D8D6E0B5
keywords:
- Método ModelName de Media Streaming API
- Media Streaming API del método ModelName, interfaz IBasicDevice
- IBasicDevice interface Media Streaming API , ModelName (método)
topic_type:
- apiref
api_name:
- IBasicDevice.ModelName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e486b372b2108bc85153f416032ef6bfbe8a397
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363531"
---
# <a name="ibasicdevicemodelname-method"></a>IBasicDevice::ModelName (método)

Recupera el nombre del modelo del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ModelName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe un puntero al nombre del modelo del dispositivo.

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

 

 





