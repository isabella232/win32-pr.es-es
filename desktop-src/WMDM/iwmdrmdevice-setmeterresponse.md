---
title: IWMDRMDevice SetMeterResponse, método
description: El método SetMeterResponse establece la respuesta de medición.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Método SetMeterResponse de Windows Media Administrador de dispositivos
- Método SetMeterResponse de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método SetMeterResponse
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699608"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a>IWMDRMDevice:: SetMeterResponse (método)

El método **SetMeterResponse** establece la respuesta de medición.

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

*pbMeterResponse* \[ de\]
</dt> <dd>

Respuesta de medición que se va a establecer.

</dd> <dt>

*cbMeterResponse* \[ de\]
</dt> <dd>

Tamaño de la respuesta de medición, en bytes.

</dd> <dt>

*pdwFlags* \[ enuncia\]
</dt> <dd>

Marcas de respuesta. Este valor debe ser uno de los siguientes marcadores.



| Marca                            | Descripción              |
|---------------------------------|--------------------------|
| \_respuesta del medidor de WMDRM \_ \_     | Todas las respuestas de medición.     |
| respuesta de medidor de WMDRM \_ \_ \_ parcial | Respuestas de medidores parciales. |



 

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

 

 





