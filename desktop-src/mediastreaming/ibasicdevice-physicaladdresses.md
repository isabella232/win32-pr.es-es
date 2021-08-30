---
title: Método IBasicDevice PhysicalAddresses
description: Devuelve un vector de direcciones físicas.
ms.assetid: 85F48EE3-14A1-46DA-A3C3-F94A8A43CF92
keywords:
- PhysicalAddresses method Media Streaming API
- PhysicalAddresses method Media Streaming API , IBasicDevice interface
- IBasicDevice interface Media Streaming API , método PhysicalAddresses
topic_type:
- apiref
api_name:
- IBasicDevice.PhysicalAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3721b7472e952d2535c892dc562125ba6d2d0ce518e8bb9c0fe7e86a4e8fb33c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011805"
---
# <a name="ibasicdevicephysicaladdresses-method"></a>IBasicDevice::P hysicalAddresses (método)

Devuelve un vector de direcciones físicas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PhysicalAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recibe una colección enumerable de punteros a direcciones físicas.

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

 

 





