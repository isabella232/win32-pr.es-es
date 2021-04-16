---
title: Método IWMDRMDeviceApp QueryDeviceStatus (WMDRMDeviceApp. h)
description: El método QueryDeviceStatus consulta el estado y las capacidades actuales de DRM de un dispositivo.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Método QueryDeviceStatus de Windows Media Administrador de dispositivos
- Método QueryDeviceStatus de Windows Media Administrador de dispositivos, interfaz IWMDRMDeviceApp
- Interfaz IWMDRMDeviceApp de Windows Media Administrador de dispositivos, método QueryDeviceStatus
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
ms.openlocfilehash: b8e0f4fad5ff9026ce70fc21712506eb4796d76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699679"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a>IWMDRMDeviceApp:: QueryDeviceStatus (método)

El método **QueryDeviceStatus** consulta el estado y las capacidades actuales de DRM de un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Puntero a un objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*pdwStatus* \[ enuncia\]
</dt> <dd>

Cero o más de los siguientes valores **DWORD** que describen los aspectos DRM del dispositivo, combinados con **una operación OR** bit a bit. Vea la sección Comentarios.



| Status                      | Descripción                                  |
|-----------------------------|----------------------------------------------|
| \_dispositivo \_ ISWMDRM de WMDRM      | El dispositivo es compatible con DRM de Windows Media.       |
| \_dispositivo \_ NEEDCLOCK de WMDRM    | El dispositivo no tiene un reloj seguro.     |
| \_dispositivo WMDRM \_ revocado      | El dispositivo se ha revocado.                 |
| \_NEEDINDIV de cliente WMDRM \_    | La seguridad de DRM debe ser individualizada. |
| \_dispositivo \_ REFRESHCLOCK de WMDRM | El reloj debe actualizarse.             |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                              | Descripción                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                     | El método se ha llevado a cabo de forma correcta.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | El argumento de entrada no es válido.<br/>                               |
| <dl> <dt>**\_ \_ \_ certificado no válido de DRM E DRM \_**</dt> </dl>          | El certificado de dispositivo recuperado del dispositivo no es válido.<br/> |
| <dl> <dt>**\_DRM E \_ DRM \_ no \_ puede \_ obtener \_ el \_ certificado del dispositivo**</dt> </dl> | No se pudo recuperar el certificado de dispositivo del dispositivo.<br/>     |



 

## <a name="remarks"></a>Observaciones

Se debe llamar a este método antes de realizar cualquier acción restringida en el contenido DRM, como transferir contenido DRM al dispositivo o adquirir información de medición. Si los valores recuperados por *pdwStatus* indican que es necesario realizar alguna acción (por ejemplo, la individualización del escritorio o la adquisición de un reloj para el dispositivo), la aplicación debe llamar a [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) y pasar el valor de *pdwStatus* recuperado de esta función al parámetro *dwFlags* en **AcquireDeviceData**. Si se devuelve cero, el dispositivo no admite Windows Media DRM 10 para dispositivos portátiles y no es necesario realizar ninguna acción. Consulte [control del contenido protegido en la aplicación](handling-protected-content-in-the-application.md) para obtener más información.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de C++ se crea un objeto **WMDRMDeviceApp** , se comprueba que el dispositivo es un dispositivo DRM 10 de Windows Media, que su reloj es preciso y, a continuación, solicita los datos de medición.


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
| Encabezado<br/>  | <dl> <dt>WMDRMDeviceApp. h (también requiere Wmdrmdeviceapp \_ i, generado a partir de WMDRMDeviceApp. idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control del contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaz IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





