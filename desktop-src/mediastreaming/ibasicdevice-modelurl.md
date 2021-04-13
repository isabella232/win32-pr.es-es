---
title: IBasicDevice ModelUrl, método
description: Recupera la dirección URL del modelo del dispositivo.
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- Método ModelUrl API de streaming de multimedia
- Método ModelUrl API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método ModelUrl
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f616d1a122f5fe6025c80742df61eb86d41514a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358077"
---
# <a name="ibasicdevicemodelurl-method"></a>IBasicDevice:: ModelUrl (método)

Recupera la dirección URL del modelo del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Recibe un puntero a la dirección URL del modelo del dispositivo.

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

 

 





