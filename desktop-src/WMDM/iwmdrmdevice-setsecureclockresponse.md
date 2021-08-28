---
title: Método IWMDRMDevice SetSecureClockResponse
description: El método SetSecureClockResponse establece la respuesta del reloj seguro.
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- Método SetSecureClockResponse windows Media Administrador de dispositivos
- Método SetSecureClockResponse windows Media Administrador de dispositivos interfaz , IWMDRMDevice
- Interfaz IWMDRMDispositivo windows Media Administrador de dispositivos , método SetSecureClockResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetSecureClockResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1af9dae5e49240ef0095f499cf8abe34d6931caf7c36cf0ec7fc6908c9821a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031865"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a>Método IWMDRMDevice::SetSecureClockResponse

El **método SetSecureClockResponse** establece la respuesta del reloj seguro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbResponse* \[ En\]
</dt> <dd>

Respuesta de reloj seguro que se va a establecer.

</dd> <dt>

*cbResponse* \[ En\]
</dt> <dd>

Tamaño especificado de la respuesta del reloj seguro, en bytes.

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

[**GetSecureClock**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**IWMDRMDevice (interfaz)**](iwmdrmdevice.md)
</dt> </dl>

 

 





