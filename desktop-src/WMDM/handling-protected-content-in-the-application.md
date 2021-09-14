---
title: Control del contenido protegido en la aplicación
description: Control del contenido protegido en la aplicación
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Windows Media Administrador de dispositivos,certificates
- Administrador de dispositivos,certificates
- guía de programación, certificados
- aplicaciones de escritorio, certificados
- crear Windows aplicaciones Administrador de dispositivos multimedia, certificados
- certificates
- Windows Contenido Administrador de dispositivos multimedia protegido por DRM
- Administrador de dispositivos contenido protegido por DRM
- guía de programación, contenido protegido por DRM
- aplicaciones de escritorio, contenido protegido por DRM
- crear Windows aplicaciones Administrador de dispositivos multimedia, contenido protegido por DRM
- Contenido protegido por DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc354e78b9c937db339f5bf6a167f504986fbb64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967859"
---
# <a name="handling-protected-content-in-the-application"></a>Control del contenido protegido en la aplicación

\[La Windows DRM multimedia está en desuso y no debe usarse. Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) en su lugar.\]

Una aplicación debe tener un certificado de transferencia para poder controlar el contenido protegido por DRM. Para obtener información sobre dónde obtener este certificado, vea [Herramientas para el desarrollo.](tools-for-development.md) Para controlar el contenido no protegido, puede usar un certificado ficticio como se describe en [Autenticación de la aplicación.](authenticating-the-application.md)

Antes de usar un dispositivo, la aplicación debe determinar si el dispositivo admite Windows Media DRM 10 para dispositivos portátiles y, si es así, si es así, si los componentes DRM están actuales. (Actual significa que el reloj seguro es correcto y que el dispositivo se ha individualizado correctamente). Si el dispositivo no admite esta versión de DRM o si no se puede actualizar, todavía puede enviar archivos al dispositivo, pero es posible que no se puedan reproducir, dependiendo de la versión de la licencia.

> [!Note]  
> Actualmente no se admite la individualización de dispositivos.

 

Si la aplicación va a vincular Windows métodos del SDK de formato multimedia, deberá vincular a la biblioteca wmStubDRM.lib de formato multimedia de Windows. Para obtener más información sobre cómo llamar Windows métodos de formato multimedia en contenido protegido con DRM, consulte "Habilitación de la compatibilidad con DRM" en la documentación del SDK Windows Media Format. Tenga en cuenta que hay un problema con la vinculación a Mssachlp.lib y WMStubDRM.lib. Esto se trata en el [artículo de KB 890079 en MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).

En el siguiente ejemplo de código de C++ se determina si un dispositivo es un dispositivo Windows Media DRM 10 y, si es así, si su reloj está actualizado.

`HRESULT IsDRMClockUpToDate()`


```C++
{
    HRESULT hr = S_OK;

    // Create the DRM handler class.
    CComPtr<IWMDRMDeviceApp> pDRM;
    hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

    // Find out first if the device is a WMDRM 10 device, and if so,
    // whether it requires clock updates.
    DWORD status = 0;
    hr = pDRM->QueryDeviceStatus(pDevice, &status);

    if (FAILED(hr)
       || (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. 
       || (status & WMDRM_DEVICE_REVOKED))   // Device is revoked.
    {
        return E_FAIL;
    }
    else if (status & WMDRM_DEVICE_NEEDCLOCK || 
        status & WMDRM_DEVICE_REFRESHCLOCK)
    {
        // Attempt update. See following example.
        hr = UpdateDRM(status);
    }
    return hr;
}
```



Si el dispositivo admite Windows Media DRM 10 para dispositivos portátiles y necesita actualizarse (es decir, si el valor de status en el ejemplo anterior no es simplemente WMDM DEVICE ISWMDRM), la aplicación debe llamar a  \_ \_ [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)  y pasar el valor de status para realizar las actualizaciones necesarias. El equipo de escritorio debe estar conectado a Internet.

La siguiente función de ejemplo de C++ intenta actualizar un dispositivo DRM.


```C++
HRESULT UpdateDRM(DWORD status)
{
    HRESULT hr = S_OK;
    hr = pDRM->AcquireDeviceData(pDevice, this, status, &result);
    if (hr != S_OK || result != 0)
    {
            return E_FAIL;
    }
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de una Windows de Administrador de dispositivos multimedia**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Control de contenido protegido**](handling-protected-content.md)
</dt> </dl>

 

 