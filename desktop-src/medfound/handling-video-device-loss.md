---
description: En este tema se describe cómo detectar la pérdida de dispositivos al usar un dispositivo de captura de vídeo.
ms.assetid: 2bffe156-c507-437e-8f32-62aaebedd6f0
title: Control de la pérdida de dispositivos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6219518d3018aae5600e66387363bbd71e29e72b83174b370bf25377c8c6b669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878957"
---
# <a name="handling-video-device-loss"></a>Control de la pérdida de dispositivos de vídeo

En este tema se describe cómo detectar la pérdida de dispositivos al usar un dispositivo de captura de vídeo. Contiene las secciones siguientes:

-   [Registro para la notificación de dispositivo](#register-for-device-notification)
-   [Obtener el vínculo simbólico del dispositivo](#get-the-symbolic-link-of-the-device)
-   [Controlar WM \_ DEVICECHANGE](/windows)
-   [Anulación del registro para notificación](#unregister-for-notification)
-   [Temas relacionados](#related-topics)

## <a name="register-for-device-notification"></a>Registro para la notificación de dispositivo

Antes de empezar a capturar desde el dispositivo, llame a la [**función RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) para registrarse para recibir notificaciones del dispositivo. Regístrese para la **clase de dispositivo KSCATEGORY \_ CAPTURE,** como se muestra en el código siguiente.


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

Enumere los dispositivos de vídeo en el sistema, como se describe [en Enumeración de dispositivos de captura de vídeo.](enumerating-video-capture-devices.md) Elija un dispositivo de la lista y, a continuación, consulte el objeto de activación para el atributo [MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ VIDCAP SYMBOLIC \_ \_ LINK,](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) como se muestra en el código siguiente.


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



## <a name="handle-wm_devicechange"></a>Controlar WM \_ DEVICECHANGE

En el bucle de mensajes, escuche los [**mensajes DE WM \_ DEVICECHANGE.**](../devio/wm-devicechange.md) El *parámetro de mensaje lParam* es un puntero a una estructura BROADCAST HDR [**\_ \_ de DEV.**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr)


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

1.  Compruebe el **miembro dbch \_ devicetype** de la estructura [**BROADCAST HDR \_ \_ de DEV.**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) Si el valor es **DBT \_ DEVTYP \_ DEVICEINTERFACE,** convierte el puntero de estructura a una estructura [**\_ DEV BROADCAST \_ DEVICEINTERFACE.**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a)
2.  Compare el **miembro dbcc \_ name** de esta estructura con el vínculo simbólico del dispositivo.


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



## <a name="unregister-for-notification"></a>Anulación del registro para notificación

Antes de que se cierre la aplicación, llame [**a UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) para anular el registro de las notificaciones del dispositivo/


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

[Enumeración de dispositivos de captura de vídeo](enumerating-video-capture-devices.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 
