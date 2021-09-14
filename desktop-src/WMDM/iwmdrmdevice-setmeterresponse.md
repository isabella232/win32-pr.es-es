---
title: Método IWMDRMDevice SetMeterResponse
description: El método SetMeterResponse establece la respuesta de medición.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Método SetMeterResponse windows Media Administrador de dispositivos
- Método SetMeterResponse windows Media Administrador de dispositivos , interfaz IWMDRMDevice
- Interfaz IWMDRMDevice windows Media Administrador de dispositivos , método SetMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed70b158215eb831296ad083af8cd2c001cb38f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967832"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a>Método IWMDRMDevice::SetMeterResponse

El **método SetMeterResponse** establece la respuesta de medición.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMeterResponse(
  [in]  BYTE  *pbMeterResponse,
  [in]  DWORD cbMeterResponse,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbMeterResponse* \[ En\]
</dt> <dd>

Respuesta de medición que se va a establecer.

</dd> <dt>

*cbMeterResponse* \[ En\]
</dt> <dd>

Tamaño de la respuesta de medición, en bytes.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Marcas de respuesta. Este valor debe ser una de las marcas siguientes.



| Marca                            | Descripción              |
|---------------------------------|--------------------------|
| RESPUESTA DE MEDIDOR WMDRM \_ \_ \_ ALL     | Todas las respuestas de medidor.     |
| WMDRM \_ METER \_ RESPONSE \_ PARTIAL | Respuestas de medidor parcial. |



 

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

 

 





