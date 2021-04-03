---
title: IBasicDevice FriendlyName (método)
description: Recupera el nombre descriptivo del dispositivo.
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- FriendlyName (método) API de streaming de multimedia
- FriendlyName Method API de streaming de media, interfaz IBasicDevice
- IBasicDevice interface media streaming API, FriendlyName (método)
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec2b2edfa3a98dfdbbdd1d236acb6e1f1433f141
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784102"
---
# <a name="ibasicdevicefriendlyname-method"></a>IBasicDevice:: FriendlyName (método)

Recupera el nombre descriptivo del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Recibe un puntero al nombre descriptivo del dispositivo.

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

 

 





