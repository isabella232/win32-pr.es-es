---
title: IBasicDevice Description (método)
description: Recupera una descripción del dispositivo.
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- Description (método) API de streaming de multimedia
- Description (método) API de streaming de media, interfaz IBasicDevice
- IBasicDevice interface media streaming API, Description (método)
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f094246d1424c458e624d4a49358b63a84b9b7d2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076622"
---
# <a name="ibasicdevicedescription-method"></a>IBasicDevice::D método Descripción

Recupera una descripción del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Recibe un puntero a la descripción del dispositivo.

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

 

 





