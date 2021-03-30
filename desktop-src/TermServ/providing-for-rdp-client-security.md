---
title: Proporcionar seguridad de cliente RDP
description: Algunas propiedades del objeto de control ActiveX Escritorio remoto están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bbb143abd3ec09a7f1aeff67a7b6dfa224b56b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775721"
---
# <a name="providing-for-rdp-client-security"></a><span data-ttu-id="8ea44-103">Proporcionar seguridad de cliente RDP</span><span class="sxs-lookup"><span data-stu-id="8ea44-103">Providing for RDP client security</span></span>

<span data-ttu-id="8ea44-104">Para permitir que los clientes se protejan de servidores potencialmente no confiables, algunas propiedades del objeto de control ActiveX Escritorio remoto están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8ea44-104">To allow clients to protect themselves from potentially untrustworthy servers, some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="8ea44-105">Esto significa que, cuando un usuario que examina la Web accede a la página y la página se encuentra en una zona de seguridad de dirección URL superior a la del equipo en el que explora la web, estas propiedades se deshabilitan.</span><span class="sxs-lookup"><span data-stu-id="8ea44-105">This means that, when a user browsing the web accesses the page and the page is in a higher URL security zone than the computer they are browsing the web with, these properties are disabled.</span></span> <span data-ttu-id="8ea44-106">Se tiene acceso a estas propiedades restringidas mediante la interfaz [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) y la interfaz [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , y están disponibles en las siguientes zonas de seguridad de direcciones URL de Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="8ea44-106">These restricted properties are accessed using the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface and the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and are available in the following Internet Explorer URL security zones:</span></span>

-   <span data-ttu-id="8ea44-107">Mi PC</span><span class="sxs-lookup"><span data-stu-id="8ea44-107">My computer</span></span>
-   <span data-ttu-id="8ea44-108">Intranet local</span><span class="sxs-lookup"><span data-stu-id="8ea44-108">Local intranet</span></span>
-   <span data-ttu-id="8ea44-109">Sitios de confianza</span><span class="sxs-lookup"><span data-stu-id="8ea44-109">Trusted sites</span></span>

<span data-ttu-id="8ea44-110">Están deshabilitadas en estas zonas:</span><span class="sxs-lookup"><span data-stu-id="8ea44-110">They are disabled in these zones:</span></span>

-   <span data-ttu-id="8ea44-111">Internet</span><span class="sxs-lookup"><span data-stu-id="8ea44-111">Internet</span></span>
-   <span data-ttu-id="8ea44-112">Sitios restringidos</span><span class="sxs-lookup"><span data-stu-id="8ea44-112">Restricted sites</span></span>

<span data-ttu-id="8ea44-113">Si llama a estas propiedades restringidas dentro de su Servicios de Escritorio remoto aplicación Web, debe llamar a [**IMsTscAx:: get \_ SecuredSettings**](imstscax-securedsettings.md) y [**IMsTscAx:: get \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) para tener acceso a las propiedades de configuración segura.</span><span class="sxs-lookup"><span data-stu-id="8ea44-113">If you call these restricted properties within your Remote Desktop Services web application, you should call [**IMsTscAx::get\_SecuredSettings**](imstscax-securedsettings.md) and [**IMsTscAx::get\_SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) to access the Secured Settings properties.</span></span>

<span data-ttu-id="8ea44-114">Las propiedades restringidas a las que tiene acceso la interfaz **IMsTscSecuredSettings** son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="8ea44-114">The restricted properties that the **IMsTscSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="8ea44-115">[**StartProgram**](imstscsecuredsettings-startprogram.md).</span><span class="sxs-lookup"><span data-stu-id="8ea44-115">[**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span> <span data-ttu-id="8ea44-116">Esta propiedad especifica el programa que se iniciará al conectarse.</span><span class="sxs-lookup"><span data-stu-id="8ea44-116">This property specifies the program that will be started upon connection.</span></span>
-   <span data-ttu-id="8ea44-117">[**WorkDir**](imstscsecuredsettings-workdir.md).</span><span class="sxs-lookup"><span data-stu-id="8ea44-117">[**WorkDir**](imstscsecuredsettings-workdir.md).</span></span> <span data-ttu-id="8ea44-118">Esta propiedad especifica el directorio de trabajo del programa especificado en [**StartProgram**](imstscsecuredsettings-startprogram.md).</span><span class="sxs-lookup"><span data-stu-id="8ea44-118">This property specifies the working directory of the program specified in [**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span>
-   <span data-ttu-id="8ea44-119">[**Pantalla completa**](imstscsecuredsettings-fullscreen.md).</span><span class="sxs-lookup"><span data-stu-id="8ea44-119">[**FullScreen**](imstscsecuredsettings-fullscreen.md).</span></span> <span data-ttu-id="8ea44-120">Esta propiedad especifica si el estado del control al conectarse estará en modo de pantalla completa o de ventana.</span><span class="sxs-lookup"><span data-stu-id="8ea44-120">This property specifies whether the state of the control upon connection will be in full-screen or window mode.</span></span> <span data-ttu-id="8ea44-121">Si el valor de esta propiedad es **true**, la conexión se abrirá en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="8ea44-121">If the value of this property is **TRUE**, the connection will be opened in full-screen mode.</span></span> <span data-ttu-id="8ea44-122">Aunque el uso de la propiedad **Fullscreen** está restringido a las zonas de seguridad de direcciones URL de Internet Explorer enumeradas anteriormente, un usuario siempre puede cambiar al modo de pantalla completa después de la conexión presionando la combinación de [teclas de método abreviado](terminal-services-shortcut-keys.md) del modo de pantalla completa (Ctrl + Alt + inter).</span><span class="sxs-lookup"><span data-stu-id="8ea44-122">Although the use of the **FullScreen** property is restricted to the Internet Explorer URL security zones listed earlier, a user can always change to full-screen mode after connection by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="8ea44-123">Las propiedades a las que accede la interfaz **IMsRdpClientSecuredSettings** son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="8ea44-123">The properties that the **IMsRdpClientSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="8ea44-124">[**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md).</span><span class="sxs-lookup"><span data-stu-id="8ea44-124">[**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md).</span></span> <span data-ttu-id="8ea44-125">Esta propiedad especifica si se deben redirigir los sonidos o reproducir sonidos en el servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="8ea44-125">This property specifies whether to redirect sounds, or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>
-   <span data-ttu-id="8ea44-126">[**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md).</span><span class="sxs-lookup"><span data-stu-id="8ea44-126">[**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md).</span></span> <span data-ttu-id="8ea44-127">Esta propiedad especifica cómo y cuándo aplicar las combinaciones de teclas de Windows; por ejemplo, ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="8ea44-127">This property specifies how and when to apply Windows key combinations; for example, ALT+TAB.</span></span>

<span data-ttu-id="8ea44-128">El siguiente script inicia Microsoft Notepad.exe tras la conexión.</span><span class="sxs-lookup"><span data-stu-id="8ea44-128">The following script launches Microsoft Notepad.exe upon connection.</span></span> <span data-ttu-id="8ea44-129">Ejecute este script antes de llamar al método [**IMsTscAx:: Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea44-129">Run this script before calling the [**IMsTscAx::Connect**](imstscax-connect.md) method.</span></span>

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




