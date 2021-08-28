---
title: Método IWMDRMDevice SetMeterResponse
description: El método SetMeterResponse establece la respuesta de medición.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Método SetMeterResponse windows Media Administrador de dispositivos
- Método SetMeterResponse windows Media Administrador de dispositivos interfaz , IWMDRMDevice
- Interfaz IWMDRMDispositivo windows Media Administrador de dispositivos , método SetMeterResponse
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
ms.openlocfilehash: b05941619d30ea067dc594e05b7b427ec5d825ef3e0c3c441cdfb3c723e94d4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619575"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a>IWMDRMDevice::SetMeterResponse (método)

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
| RESPUESTA DE MEDIDOR WMDRM \_ \_ \_ TODO     | Todas las respuestas de medidor.     |
| RESPUESTA PARCIAL DEL MEDIDOR WMDRM \_ \_ \_ | Respuestas de medidor parcial. |



 

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

 

 





