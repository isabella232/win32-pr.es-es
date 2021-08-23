---
title: Método IWMDRMDeviceApp QueryDeviceStatus (WMDRMDeviceApp.h)
description: El método QueryDeviceStatus consulta a un dispositivo su estado y funcionalidades actuales de DRM.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Método QueryDeviceStatus windows Media Administrador de dispositivos
- Método QueryDeviceStatus de Windows Media Administrador de dispositivos , interfaz IWMDRMDeviceApp
- Interfaz IWMDRMDeviceApp windows Media Administrador de dispositivos , método QueryDeviceStatus
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.QueryDeviceStatus
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b169412104a5e22ae973542457d08bead328ea4ded5a34691499ea8dbfd8b7b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055652"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a>IWMDRMDeviceApp::QueryDeviceStatus (método)

El **método QueryDeviceStatus** consulta a un dispositivo su estado y funcionalidades actuales de DRM.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Puntero a un [**objeto IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)

</dd> <dt>

*pdwStatus* \[ out\]
</dt> <dd>

Cero o más de los siguientes valores **DWORD** que describen los aspectos de DRM del dispositivo, combinados con un OR bit a **bit.** Vea la sección Comentarios.



| Status                      | Descripción                                  |
|-----------------------------|----------------------------------------------|
| \_ISWMDRM DE DISPOSITIVO \_ WMDRM      | El dispositivo admite Windows DRM multimedia.       |
| \_NEEDCLOCK DEL DISPOSITIVO \_ WMDRM    | El dispositivo no tiene un reloj seguro.     |
| DISPOSITIVO WMDRM \_ \_ REVOCADO      | Se ha revocado el dispositivo.                 |
| NECESIDAD DE CLIENTE \_ \_ WMDRMINDIV    | La seguridad de DRM debe individualizarse. |
| ACTUALIZACIÓN DE \_ DISPOSITIVO \_ WMDRMCLOCK | El reloj debe actualizarse.             |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                              | Descripción                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                     | El método se ha llevado a cabo de forma correcta.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | El argumento de entrada no es válido.<br/>                               |
| <dl> <dt>**CERTIFICADO NO VÁLIDO DE DRM DE NS \_ \_ \_ \_ E**</dt> </dl>          | El certificado de dispositivo recuperado del dispositivo no es válido.<br/> |
| <dl> <dt>**NS \_ E DRM NO PUEDE OBTENER EL CERTIFICADO DE \_ \_ \_ \_ \_ \_ DISPOSITIVO**</dt> </dl> | No se pudo recuperar el certificado de dispositivo del dispositivo.<br/>     |



 

## <a name="remarks"></a>Comentarios

Se debe llamar a este método antes de realizar acciones restringidas en el contenido DRM, como transferir contenido DRM al dispositivo o adquirir información de medición. Si los valores recuperados por *pdwStatus* indican que es necesario realizar alguna acción (como la individualización para el escritorio o la adquisición de un reloj para el dispositivo), la aplicación debe llamar a [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) y pasar el valor *pdwStatus* recuperado de esta función al parámetro *dwFlags* **en AcquireDeviceData.** Si se devuelve cero, el dispositivo no admite Windows DRM multimedia 10 para dispositivos portátiles y no es necesario realizar ninguna acción. Consulte [Control de contenido protegido en la aplicación para](handling-protected-content-in-the-application.md) obtener más información.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de C++ se crea un objeto **WMDRMDeviceApp,** se comprueba que el dispositivo es un dispositivo DRM 10 multimedia de Windows, que su reloj es preciso y, a continuación, solicita los datos de medición.


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
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDRMDeviceApp.h (también requiere Wmdrmdeviceapp \_ i.c, creado a partir de WMDRMDeviceApp.idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control del contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaz IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





