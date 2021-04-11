---
description: Omite el número especificado de dispositivos en la secuencia de enumeración.
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: 'IEnumPortableDeviceConnectors:: Skip (método) (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Skip
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: c00daecccd12beee8e9e741c2906e47484fa6da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083008"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a>IEnumPortableDeviceConnectors:: Skip (método)

El método **SKIP** omite el número especificado de dispositivos en la secuencia de enumeración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cConnectors* \[ de\]
</dt> <dd>

El número de dispositivos que se van a omitir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                             | Descripción                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>    | El método se ha llevado a cabo de forma correcta.<br/>                                                                                                                                                          |
| <dl> <dt>**S \_ false**</dt> </dl> | No se pudo omitir el número especificado de dispositivos. Una posible causa: el parámetro *cConnectors* especifica más dispositivos que los que permanecen realmente en la secuencia de enumeración.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                                                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                                   |
| Encabezado<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Portabledeviceconnectapi. idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




