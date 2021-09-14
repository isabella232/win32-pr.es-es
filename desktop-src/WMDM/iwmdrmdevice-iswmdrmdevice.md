---
title: Método IWMDRMDevice IsWMDRMDevice
description: El método IsWMDRMDevice determina si el dispositivo admite Windows DRM multimedia 10 para dispositivos portátiles.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Método IsWMDRMDevice windows Media Administrador de dispositivos
- Método IsWMDRMDevice windows Media Administrador de dispositivos , interfaz IWMDRMDevice
- Interfaz IWMDRMDevice windows Media Administrador de dispositivos , método IsWMDRMDevice
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
ms.openlocfilehash: ca9cb79598ea41a996748e383c8fdfc63364dd6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967823"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a>IWMDRMDevice::IsWMDRMDevice (método)

El **método IsWMDRMDevice** determina si el dispositivo admite Windows DRM multimedia 10 para dispositivos portátiles.

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

Versión de Windows Drm multimedia 10 para dispositivos portátiles, que tiene el valor de 0x00010000.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





