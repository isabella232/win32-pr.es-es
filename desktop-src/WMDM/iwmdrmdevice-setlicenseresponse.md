---
title: Método IWMDRMDevice SetLicenseResponse
description: El método SetLicenseResponse establece la respuesta de la licencia.
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- Método SetLicenseResponse windows Media Administrador de dispositivos
- Método SetLicenseResponse windows Media Administrador de dispositivos , interfaz IWMDRMDevice
- Interfaz IWMDRMDispositivo windows Media Administrador de dispositivos , método SetLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetLicenseResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4161732002378449f196fdf83c4b880fcc2c02d345a0b08c6e6a464b81acb1dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055723"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a>IWMDRMDevice::SetLicenseResponse (método)

El **método SetLicenseResponse** establece la respuesta de licencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbResponse* \[ En\]
</dt> <dd>

Especifica la respuesta que se va a establecer.

</dd> <dt>

*cbResponse* \[ En\]
</dt> <dd>

Tamaño de la respuesta, en bytes.

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

 

 





