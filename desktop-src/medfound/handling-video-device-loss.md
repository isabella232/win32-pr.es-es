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
# <a name="handling-video-device-loss"></a><span data-ttu-id="8cc09-103">Controlar la pérdida de dispositivos de vídeo</span><span class="sxs-lookup"><span data-stu-id="8cc09-103">Handling Video Device Loss</span></span>

<span data-ttu-id="8cc09-104">En este tema se describe cómo detectar la pérdida de dispositivos cuando se usa un dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8cc09-104">This topic describes how to detect device loss when using a video capture device.</span></span> <span data-ttu-id="8cc09-105">Contiene las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="8cc09-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="8cc09-106">Registrar para recibir notificaciones de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8cc09-106">Register For Device Notification</span></span>](#register-for-device-notification)
-   [<span data-ttu-id="8cc09-107">Obtener el vínculo simbólico del dispositivo</span><span class="sxs-lookup"><span data-stu-id="8cc09-107">Get the Symbolic Link of the Device</span></span>](#get-the-symbolic-link-of-the-device)
-   [<span data-ttu-id="8cc09-108">Administrar DEVICECHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="8cc09-108">Handle WM\_DEVICECHANGE</span></span>](/windows)
-   [<span data-ttu-id="8cc09-109">Anular el registro de la notificación</span><span class="sxs-lookup"><span data-stu-id="8cc09-109">Unregister For Notification</span></span>](#unregister-for-notification)
-   [<span data-ttu-id="8cc09-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8cc09-110">Related topics</span></span>](#related-topics)

## <a name="register-for-device-notification"></a><span data-ttu-id="8cc09-111">Registrar para recibir notificaciones de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8cc09-111">Register For Device Notification</span></span>

<span data-ttu-id="8cc09-112">Antes de iniciar la captura desde el dispositivo, llame a la función [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) para registrarse para recibir notificaciones de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8cc09-112">Before you start capturing from the device, call the [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) function to register for device notifications.</span></span> <span data-ttu-id="8cc09-113">Regístrese para la clase de dispositivo de **\_ captura KSCATEGORY** , tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="8cc09-113">Register for the **KSCATEGORY\_CAPTURE** device class, as shown in the following code.</span></span>


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



## <a name="get-the-symbolic-link-of-the-device"></a><span data-ttu-id="8cc09-114">Obtener el vínculo simbólico del dispositivo</span><span class="sxs-lookup"><span data-stu-id="8cc09-114">Get the Symbolic Link of the Device</span></span>

<span data-ttu-id="8cc09-115">Enumerar los dispositivos de vídeo en el sistema, como se describe en [enumeración](enumerating-video-capture-devices.md)de los dispositivos de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8cc09-115">Enumerate the video devices on the system, as described in [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span> <span data-ttu-id="8cc09-116">Elija un dispositivo de la lista y, a continuación, consulte el objeto de activación para el [tipo de origen del atributo MF DEVSOURCE atributo de \_ \_ \_ \_ \_ \_ \_ vínculo de VIDCAP](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) , tal como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="8cc09-116">Choose a device from the list, and then query the activation object for the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute, as shown in the following code.</span></span>


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



## <a name="handle-wm_devicechange"></a><span data-ttu-id="8cc09-117">Administrar DEVICECHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="8cc09-117">Handle WM\_DEVICECHANGE</span></span>

<span data-ttu-id="8cc09-118">En el bucle de mensajes, escuche los mensajes de [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="8cc09-118">In your message loop, listen for [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) messages.</span></span> <span data-ttu-id="8cc09-119">El parámetro de mensaje *lParam* es un puntero a una estructura [**\_ \_ HDR broadcast de dev**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) .</span><span class="sxs-lookup"><span data-stu-id="8cc09-119">The *lParam* message parameter is a pointer to a [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span>


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



<span data-ttu-id="8cc09-120">A continuación, compare el mensaje de notificación del dispositivo con el vínculo simbólico del dispositivo, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8cc09-120">Next, compare the device notification message against the symbolic link of your device, as follows:</span></span>

1.  <span data-ttu-id="8cc09-121">Compruebe el miembro de **dbch \_ DeviceType** de la estructura de [**\_ \_ HDR de dev Broadcast**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) .</span><span class="sxs-lookup"><span data-stu-id="8cc09-121">Check the **dbch\_devicetype** member of the [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="8cc09-122">Si el valor es **DBT \_ DEVTYP \_ deviceinterface**, convierta el puntero de estructura a una estructura [**dev \_ Broadcast \_ DEVICEINTERFACE**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) .</span><span class="sxs-lookup"><span data-stu-id="8cc09-122">If the value is **DBT\_DEVTYP\_DEVICEINTERFACE**, cast the structure pointer to a [**DEV\_BROADCAST\_DEVICEINTERFACE**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) structure.</span></span>
2.  <span data-ttu-id="8cc09-123">Compare el miembro **DBCC \_ Name** de esta estructura con el vínculo simbólico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8cc09-123">Compare the **dbcc\_name** member of this structure to the symbolic link of the device.</span></span>


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



## <a name="unregister-for-notification"></a><span data-ttu-id="8cc09-124">Anular el registro de la notificación</span><span class="sxs-lookup"><span data-stu-id="8cc09-124">Unregister For Notification</span></span>

<span data-ttu-id="8cc09-125">Antes de que se cierre la aplicación, llame a [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) para anular el registro de las notificaciones de dispositivo/</span><span class="sxs-lookup"><span data-stu-id="8cc09-125">Before the application exits, call [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) to unregister for device notifications/</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8cc09-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8cc09-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cc09-127">Enumerar dispositivos de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="8cc09-127">Enumerating Video Capture Devices</span></span>](enumerating-video-capture-devices.md)
</dt> <dt>

[<span data-ttu-id="8cc09-128">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="8cc09-128">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
