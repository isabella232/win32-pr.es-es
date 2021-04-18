---
title: IWMDRMDevice SetLicenseResponse, método
description: El método SetLicenseResponse establece la respuesta de la licencia.
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- Método SetLicenseResponse de Windows Media Administrador de dispositivos
- Método SetLicenseResponse de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método SetLicenseResponse
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
ms.openlocfilehash: f32a2d27fabe45081b13d658e49171af035b8cc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699611"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a>IWMDRMDevice:: SetLicenseResponse (método)

El método **SetLicenseResponse** establece la respuesta de la licencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbResponse* \[ de\]
</dt> <dd>

Especifica la respuesta que se va a establecer.

</dd> <dt>

*cbResponse* \[ de\]
</dt> <dd>

Tamaño de la respuesta, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





