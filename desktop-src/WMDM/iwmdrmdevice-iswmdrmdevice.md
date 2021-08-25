---
title: Método IWMDRMDevice IsWMDRMDevice
description: El método IsWMDRMDevice determina si el dispositivo admite Windows Drm multimedia 10 para dispositivos portátiles.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Método IsWMDRMDevice windows Media Administrador de dispositivos
- Método IsWMDRMDevice windows Media Administrador de dispositivos interfaz , IWMDRMDevice
- Interfaz IWMDRMDevice windows Media Administrador de dispositivos método , IsWMDRMDevice
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60ee225267ce2301e9a2dad392d72ce72b0e698872cd3fd54ab3e50a07043477
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957265"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a>IWMDRMDevice::IsWMDRMDevice (método)

El **método IsWMDRMDevice** determina si el dispositivo admite Windows DRM 10 multimedia para dispositivos portátiles.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdwVersion* \[ out\]
</dt> <dd>

Versión de Windows DRM 10 de multimedia para dispositivos portátiles, que tiene el valor de 0x00010000.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMDevice (interfaz)**](iwmdrmdevice.md)
</dt> </dl>

 

 





