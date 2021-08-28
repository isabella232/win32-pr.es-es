---
title: Método IWMDRMDeviceApp ProcessMeterResponse (WMDRMDeviceApp.h)
description: El método ProcessMeterResponse restablece algunos o todos los recuentos de medición de un dispositivo, después de que el servidor haya enviado y procesado los datos del dispositivo.
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- Método ProcessMeterResponse windows Media Administrador de dispositivos
- Método ProcessMeterResponse windows Media Administrador de dispositivos , interfaz IWMDRMDeviceApp
- IWMDRMDeviceApp interface windows Media Administrador de dispositivos , ProcessMeterResponse method
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
ms.openlocfilehash: 20e20338482533293559f135a221b90220f1e371137b3bc1d62502cb3f2e779b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766455"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a>Método IWMDRMDeviceApp::P rocessMeterResponse

El **método ProcessMeterResponse** restablece algunos o todos los recuentos de medición de un dispositivo, después de que el servidor haya enviado y procesado los datos del dispositivo.

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

*pDevice* \[ En\]
</dt> <dd>

Puntero a un [**objeto IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)

</dd> <dt>

*pbResponse* \[ En\]
</dt> <dd>

Respuesta recibida de un servidor de medición, después de enviar los datos generados [**mediante GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).

</dd> <dt>

*cbResponse* \[ En\]
</dt> <dd>

Tamaño de *pbResponse,* en bytes.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

DWORD **de** la tabla siguiente que indica si hay más datos de medición en el dispositivo que deben procesarse.



| Marca                            | Descripción                                     |
|---------------------------------|-------------------------------------------------|
| RESPUESTA DE MEDIDOR WMDRM \_ \_ \_ TODO     | Se han procesado todos los datos de medición.           |
| RESPUESTA PARCIAL DEL MEDIDOR WMDRM \_ \_ \_ | Es necesario procesar datos de medición adicionales. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                      | Descripción                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                             | El método se ha llevado a cabo de forma correcta.<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | Uno o varios argumentos no son válidos.<br/>                               |
| <dl> <dt>**Errores del dispositivo**</dt> </dl>            | Cualquiera de varios errores de dispositivo.<br/>                                  |
| <dl> <dt>**Errores del cliente DRM**</dt> </dl>        | Cualquiera de varios errores de cliente DRM internos.<br/>                     |
| <dl> <dt>**NS \_ E \_ DEVICE \_ NOT \_ WMDRM \_ DEVICE**</dt> </dl> | El dispositivo especificado no es un dispositivo compatible Windows DRM multimedia.<br/> |



 

## <a name="remarks"></a>Comentarios

Puede encontrar más información sobre la medición, incluidos ejemplos de código, en las whitepaper [Metering the Use of Digital Media Content with Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) (Medición del uso de contenido multimedia digital con DRM 10 de medios de Windows) en el sitio web de MSDN.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDRMDeviceApp.h (también requiere Wmdrmdeviceapp i.c, creado a partir de \_ WMDRMDeviceApp.idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control de contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDMDevice (interfaz)**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**IWMDRMDeviceApp (interfaz)**](iwmdrmdeviceapp.md)
</dt> </dl>

 

