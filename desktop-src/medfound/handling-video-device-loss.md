---
description: En este tema se describe cómo detectar la pérdida de dispositivos cuando se usa un dispositivo de captura de vídeo.
ms.assetid: 2bffe156-c507-437e-8f32-62aaebedd6f0
title: Controlar la pérdida de dispositivos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d083ebeb1203b0bba49a63745f62a4dff6b231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715448"
---
# <a name="handling-video-device-loss"></a>Controlar la pérdida de dispositivos de vídeo

En este tema se describe cómo detectar la pérdida de dispositivos cuando se usa un dispositivo de captura de vídeo. Contiene las secciones siguientes:

-   [Registrar para recibir notificaciones de dispositivo](#register-for-device-notification)
-   [Obtener el vínculo simbólico del dispositivo](#get-the-symbolic-link-of-the-device)
-   [Administrar DEVICECHANGE de WM \_](/windows)
-   [Anular el registro de la notificación](#unregister-for-notification)
-   [Temas relacionados](#related-topics)

## <a name="register-for-device-notification"></a>Registrar para recibir notificaciones de dispositivo

Antes de iniciar la captura desde el dispositivo, llame a la función [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) para registrarse para recibir notificaciones de dispositivo. Regístrese para la clase de dispositivo de **\_ captura KSCATEGORY** , tal y como se muestra en el código siguiente.


```C++
#include <Dbt.h>
#include <ks.h>
#include <ksmedia.h>

HDEVNOTIFY  g_hdevnotify = NULL;

BOOL RegisterForDeviceNotification(HWND hwnd)
{
    DEV_BROADCAST_DEVICEINTERFACE di = { 0 };
    di.dbcc_size = sizeof(di);
    di.dbcc_devicetype  = DBT_DEVTYP_DEVICEINTERFACE;
    di.dbcc_classguid  = KSCATEGORY_CAPTURE; 

    g_hdevnotify = RegisterDeviceNotification(
        hwnd,
        &di,
        DEVICE_NOTIFY_WINDOW_HANDLE
        );

    if (g_hdevnotify == NULL)
    {
        return FALSE;
    }

    return TRUE;
}
```



## <a name="get-the-symbolic-link-of-the-device"></a>Obtener el vínculo simbólico del dispositivo

Enumerar los dispositivos de vídeo en el sistema, como se describe en [enumeración](enumerating-video-capture-devices.md)de los dispositivos de captura de vídeo. Elija un dispositivo de la lista y, a continuación, consulte el objeto de activación para el [tipo de origen del atributo MF DEVSOURCE atributo de \_ \_ \_ \_ \_ \_ \_ vínculo de VIDCAP](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) , tal como se muestra en el código siguiente.


```C++
WCHAR      *g_pwszSymbolicLink = NULL;
UINT32     g_cchSymbolicLink = 0;

HRESULT GetSymbolicLink(IMFActivate *pActivate)
{
    return pActivate->GetAllocatedString(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
        &g_pwszSymbolicLink,
        &g_cchSymbolicLink
        );
}
```



## <a name="handle-wm_devicechange"></a>Administrar DEVICECHANGE de WM \_

En el bucle de mensajes, escuche los mensajes de [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) . El parámetro de mensaje *lParam* es un puntero a una estructura [**\_ \_ HDR broadcast de dev**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) .


```C++
    case WM_DEVICECHANGE:
        if (lParam != 0)
        {
            HRESULT hr = S_OK;
            BOOL bDeviceLost = FALSE;

            hr = CheckDeviceLost((PDEV_BROADCAST_HDR)lParam, &bDeviceLost);

            if (FAILED(hr) || bDeviceLost)
            {
                CloseDevice();

                MessageBox(hwnd, L"Lost the capture device.", NULL, MB_OK);
            }
        }
        return TRUE;
```



A continuación, compare el mensaje de notificación del dispositivo con el vínculo simbólico del dispositivo, como se indica a continuación:

1.  Compruebe el miembro de **dbch \_ DeviceType** de la estructura de [**\_ \_ HDR de dev Broadcast**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) . Si el valor es **DBT \_ DEVTYP \_ deviceinterface**, convierta el puntero de estructura a una estructura [**dev \_ Broadcast \_ DEVICEINTERFACE**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) .
2.  Compare el miembro **DBCC \_ Name** de esta estructura con el vínculo simbólico del dispositivo.


```C++
HRESULT CheckDeviceLost(DEV_BROADCAST_HDR *pHdr, BOOL *pbDeviceLost)
{
    DEV_BROADCAST_DEVICEINTERFACE *pDi = NULL;

    if (pbDeviceLost == NULL)
    {
        return E_POINTER;
    }

    *pbDeviceLost = FALSE;
    
    if (g_pSource == NULL)
    {
        return S_OK;
    }
    if (pHdr == NULL)
    {
        return S_OK;
    }
    if (pHdr->dbch_devicetype != DBT_DEVTYP_DEVICEINTERFACE)
    {
        return S_OK;
    }

    // Compare the device name with the symbolic link.

    pDi = (DEV_BROADCAST_DEVICEINTERFACE*)pHdr;

    if (g_pwszSymbolicLink)
    {
        if (_wcsicmp(g_pwszSymbolicLink, pDi->dbcc_name) == 0)
        {
            *pbDeviceLost = TRUE;
        }
    }

    return S_OK;
}
```



## <a name="unregister-for-notification"></a>Anular el registro de la notificación

Antes de que se cierre la aplicación, llame a [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) para anular el registro de las notificaciones de dispositivo/


```C++
void OnClose(HWND /*hwnd*/)
{
    if (g_hdevnotify)
    {
        UnregisterDeviceNotification(g_hdevnotify);
    }

    PostQuitMessage(0);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumerar dispositivos de captura de vídeo](enumerating-video-capture-devices.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 
