---
title: Método IWMDRMDeviceApp ProcessMeterResponse (WMDRMDeviceApp. h)
description: El método ProcessMeterResponse restablece algunos o todos los recuentos de disponibilidad en un dispositivo, después de que el servidor haya enviado y procesado los datos del dispositivo.
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- Método ProcessMeterResponse de Windows Media Administrador de dispositivos
- Método ProcessMeterResponse de Windows Media Administrador de dispositivos, interfaz IWMDRMDeviceApp
- Interfaz IWMDRMDeviceApp de Windows Media Administrador de dispositivos, método ProcessMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.ProcessMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b57312dc2f401207e41f38f5bf75cddf69a13b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699680"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a>IWMDRMDeviceApp::P método rocessMeterResponse

El método **ProcessMeterResponse** restablece algunos o todos los recuentos de disponibilidad en un dispositivo, después de que el servidor haya enviado y procesado los datos del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ProcessMeterResponse(
  [in]  IWMDMDevice *pDevice,
  [in]  BYTE        *pbResponse,
  [in]  DWORD       cbResponse,
  [out] DWORD       *pdwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Puntero a un objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*pbResponse* \[ de\]
</dt> <dd>

Respuesta recibida de un servidor de disponibilidad, después de enviar los datos generados con [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).

</dd> <dt>

*cbResponse* \[ de\]
</dt> <dd>

Tamaño de *pbResponse*, en bytes.

</dd> <dt>

*pdwFlags* \[ enuncia\]
</dt> <dd>

Un **valor DWORD** de la siguiente tabla que indica si hay más datos de disponibilidad en el dispositivo que se deben procesar.



| Marca                            | Descripción                                     |
|---------------------------------|-------------------------------------------------|
| \_respuesta del medidor de WMDRM \_ \_     | Se han procesado todos los datos de medición.           |
| respuesta de medidor de WMDRM \_ \_ \_ parcial | Es necesario procesar datos de medición adicionales. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                      | Descripción                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                             | El método se ha llevado a cabo de forma correcta.<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | Uno o varios argumentos no son válidos.<br/>                               |
| <dl> <dt>**Errores del dispositivo**</dt> </dl>            | Cualquier número de errores de dispositivo.<br/>                                  |
| <dl> <dt>**Errores del cliente DRM**</dt> </dl>        | Cualquiera de los errores internos del cliente DRM.<br/>                     |
| <dl> <dt>**dispositivo \_ E \_ dispositivo \_ no \_ WMDRM \_**</dt> </dl> | El dispositivo especificado no es un dispositivo compatible con DRM de Windows Media.<br/> |



 

## <a name="remarks"></a>Observaciones

Puede encontrar más información sobre la medición, incluidos ejemplos de código, en las notas del producto sobre [el uso de contenido multimedia digital con Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) en el sitio web de MSDN.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDRMDeviceApp. h (también requiere Wmdrmdeviceapp \_ i, generado a partir de WMDRMDeviceApp. idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control del contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaz IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**Interfaz IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

