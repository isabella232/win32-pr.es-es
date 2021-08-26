---
description: Crea una copia de la interfaz IEnumPortableDeviceConnectors actual.
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
title: Método IEnumPortableDeviceConnectors::Clone (Devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Clone
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 53b9c49b5bf36571409cd49026d5d08fced80c3e43aee63d844abd481e51aa3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055335"
---
# <a name="ienumportabledeviceconnectorsclone-method"></a>IEnumPortableDeviceConnectors::Clone (Método)

El **método Clone** crea una copia de la interfaz [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumPortableDeviceConnectors **ppEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Dirección de un puntero a una [**interfaz IEnumPortableDeviceConnectors.**](ienumportabledeviceconnectors.md) La aplicación que realiza la llamada debe liberar esta interfaz cuando haya terminado con ella.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                                                                             |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




