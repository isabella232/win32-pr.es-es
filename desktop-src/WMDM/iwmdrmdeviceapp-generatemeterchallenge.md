---
title: Método IWMDRMDeviceApp GenerateMeterChallenge (WMDRMDeviceApp.h)
description: El método GenerateMeterChallenge adquiere datos de medición de un dispositivo.
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- Método GenerateMeterChallenge windows Media Administrador de dispositivos
- Método GenerateMeterChallenge windows Media Administrador de dispositivos interfaz , IWMDRMDeviceApp
- IWMDRMDeviceApp interface windows Media Administrador de dispositivos , GenerateMeterChallenge method
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.GenerateMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e91ac5049740d360ae0c5f53959b3d952188bfa2a569c58a9e7cf86ae0c22577
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584554"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a>IWMDRMDeviceApp::GenerateMeterChallenge (método)

El **método GenerateMeterChallenge** adquiere datos de medición de un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Puntero a una [**interfaz IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) Si la aplicación pasa **NULL,** se usa la información de medición almacenada en el equipo en lugar de la información de medición de un dispositivo conectado.

</dd> <dt>

*bstrMeterCert* \[ En\]
</dt> <dd>

Certificado de medición de la aplicación, como **BSTR**. Se trata de un certificado firmado recibido de Microsoft.

</dd> <dt>

*pbstrMeterURL* \[ out\]
</dt> <dd>

Dirección URL a la que se deben enviar los datos de medición. Esto se asigna mediante Windows media Administrador de dispositivos y el autor de la llamada debe liberarlo **mediante SysFreeString.**

</dd> <dt>

*pbstrMeterData* \[ out\]
</dt> <dd>

Datos de medición que se enviarán al servicio de medición. Esto se asigna mediante Windows media Administrador de dispositivos y el autor de la llamada debe liberarlo **mediante SysFreeString.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                      | Descripción                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                             | El método se ha llevado a cabo de forma correcta.<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | Uno o varios argumentos no son válidos.<br/>                               |
| <dl> <dt>**DRM \_ E \_ INVALIDXMLTAG**</dt> </dl>             | XML tiene un formato incorrecto.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt> </dl>             | XML tiene un formato incorrecto.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ NOXMLOPENTAG**</dt> </dl>              | XML tiene un formato incorrecto.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ XMLNOTFOUND**</dt> </dl>               | No se pudo encontrar una etiqueta XML necesaria.<br/>                                 |
| <dl> <dt>**Errores del dispositivo**</dt> </dl>            | Cualquiera de varios errores de dispositivo.<br/>                                  |
| <dl> <dt>**Errores del cliente DRM**</dt> </dl>        | Cualquiera de varios errores de cliente DRM internos.<br/>                     |
| <dl> <dt>**NS \_ E \_ DEVICE \_ NOT \_ WMDRM \_ DEVICE**</dt> </dl> | El dispositivo especificado no es un dispositivo compatible Windows DRM multimedia.<br/> |



 

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, la aplicación debe llamar a [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) para comprobar que todos los componentes DRM del dispositivo están actualizados. Solo se puede llamar a este método en un dispositivo que admita Windows DRM 10 multimedia para dispositivos portátiles.

Los datos recuperados *pbstrMeterData* deben enviarse a la dirección URL especificada por *pbstrMeterURL.* Asegúrese de codificar mediante URL los datos recuperados para que no se modifiquen durante la transferencia.

Consulte [Control de contenido protegido en la aplicación para](handling-protected-content-in-the-application.md) obtener más información.

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código de C++ crea un objeto **WMDRMDeviceApp,** comprueba que el dispositivo es un dispositivo DRM 10 de Windows Media, que su reloj es preciso y, a continuación, solicita los datos de medición.


```C++
HRESULT hr = S_OK;
// Create the WMDRMDeviceApp object.
CComPtr<IWMDRMDeviceApp> pDRM;
hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

// Find out first if the device is a WMDRM 10 device, and if it requires
// any clock updates.
DWORD status = 0;
hr = pDRM->QueryDeviceStatus(pDevice, &status);

if (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. Nothing can be updated,
    return E_FAIL;                   // and metering cannot be performed.
else if (status & WMDRM_DEVICE_REVOKED) // Device is revoked.
    return E_FAIL;
else if (status & WMDRM_DEVICE_NEEDCLOCK || 
    status & WMDRM_CLIENT_NEEDINDIV ||
    status & WMDRM_DEVICE_REFRESHCLOCK)
{
    // Need to update device clock. 
    // Using custom function, which is synchronous.
    hr = myAcquireDeviceData(pDRM, pDevice, this, status, &result);
    if (hr != S_OK || result != 0)    // Couldn't perform the updates.
        return E_FAIL;    
}

// Any updates have been performed. Now get the metering information from the device.
CComBSTR meterCert(METERCERT);
CComBSTR URL;
CComBSTR rawdata;
CComBSTR data;
hr = pDRM->GenerateMeterChallenge(pDevice, meterCert, &URL, &rawdata);
if (hr == S_OK)
    ..... Send to URL...
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDRMDeviceApp.h (también requiere Wmdrmdeviceapp i.c, creado a partir de \_ WMDRMDeviceApp.idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Control de contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDMDevice (interfaz)**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**IWMDRMDeviceApp (interfaz)**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





