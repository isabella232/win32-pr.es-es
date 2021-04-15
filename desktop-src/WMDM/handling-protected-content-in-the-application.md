---
title: Control del contenido protegido en la aplicación
description: Control del contenido protegido en la aplicación
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Windows Media Administrador de dispositivos, certificados
- Administrador de dispositivos, certificados
- Guía de programación, certificados
- aplicaciones de escritorio, certificados
- crear aplicaciones de Windows Media Administrador de dispositivos, certificados
- certificates
- Windows Media Administrador de dispositivos, contenido protegido con DRM
- Administrador de dispositivos, contenido protegido con DRM
- Guía de programación, contenido protegido con DRM
- aplicaciones de escritorio, contenido protegido con DRM
- creación de aplicaciones de Windows Media Administrador de dispositivos, contenido protegido con DRM
- Contenido protegido con DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc354e78b9c937db339f5bf6a167f504986fbb64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695701"
---
# <a name="handling-protected-content-in-the-application"></a>Control del contenido protegido en la aplicación

\[La característica Windows Media DRM está en desuso y no debe usarse. En su lugar, use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

Una aplicación debe tener un certificado de transferencia para poder controlar el contenido protegido con DRM. Para obtener información sobre dónde obtener este certificado, vea [herramientas para el desarrollo](tools-for-development.md). Para controlar el contenido no protegido, puede usar un certificado ficticio tal y como se describe en [autenticación de la aplicación](authenticating-the-application.md).

Antes de usar un dispositivo, la aplicación debe determinar si el dispositivo es compatible con Windows Media DRM 10 para dispositivos portátiles y, en caso afirmativo, que los componentes de DRM estén actualizados. (Actual significa que el reloj seguro es correcto y que el dispositivo se ha individualizado correctamente). Si el dispositivo no es compatible con esta versión de DRM, o si no se puede actualizar, todavía puede enviar archivos al dispositivo, pero es posible que no se puedan reproducir, dependiendo de la versión de licencia.

> [!Note]  
> Actualmente no se admite la individualización de dispositivos.

 

Si la aplicación va a vincularse a los métodos del SDK de Windows Media Format, deberá vincular a la biblioteca de formato de Windows Media WMStubDRM. lib. Para obtener más información sobre cómo llamar a los métodos de formato de Windows Media en contenido protegido con DRM, vea "habilitar la compatibilidad con DRM" en la documentación del SDK de Windows Media Format. Tenga en cuenta que hay un problema con la vinculación a Mssachlp. lib y WMStubDRM. lib. Esto se trata en el [artículo 890079 de Knowledge base en MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).

En el siguiente ejemplo de código de C++ se determina si un dispositivo es un dispositivo DRM 10 de Windows Media y, en caso afirmativo, que su reloj está actualizado.

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



Si el dispositivo es compatible con Windows Media DRM 10 para dispositivos portátiles y debe actualizarse (es decir, si el valor de *status* en el ejemplo anterior no es simplemente \_ dispositivo WMDM \_ ISWMDRM), la aplicación debe llamar a [**IWMDRMDeviceApp:: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) y pasar el valor de *status* para realizar las actualizaciones necesarias. El equipo de escritorio debe estar conectado a Internet.

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

[**Crear una aplicación de Windows Media Administrador de dispositivos**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Control de contenido protegido**](handling-protected-content.md)
</dt> </dl>

 

 