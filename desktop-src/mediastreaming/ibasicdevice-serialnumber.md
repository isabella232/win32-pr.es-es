---
title: IBasicDevice SerialNumber (método)
description: Recupera el número de serie del dispositivo.
ms.assetid: 238A5999-0E8B-4462-AFCF-790DB58CFCB4
keywords:
- Método SerialNumber API de streaming de multimedia
- Método SerialNumber API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice streaming de multimedia API, método SerialNumber
topic_type:
- apiref
api_name:
- IBasicDevice.SerialNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f24fad2e74c3ec2a5b489d8f5dd57265ea6d21bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358089"
---
# <a name="ibasicdeviceserialnumber-method"></a>IBasicDevice:: SerialNumber (método)

Recupera el número de serie del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SerialNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Recibe un puntero al número de serie del dispositivo.

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

 

 





