---
title: Creación de estación de ventana y escritorio
description: El sistema crea automáticamente la estación de ventana interactiva.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aff24a29432e3e394a199bf881aa386bf17e71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104358976"
---
# <a name="window-station-and-desktop-creation"></a><span data-ttu-id="6d435-103">Creación de estación de ventana y escritorio</span><span class="sxs-lookup"><span data-stu-id="6d435-103">Window Station and Desktop Creation</span></span>

<span data-ttu-id="6d435-104">El sistema crea automáticamente la estación de ventana interactiva.</span><span class="sxs-lookup"><span data-stu-id="6d435-104">The system automatically creates the interactive window station.</span></span> <span data-ttu-id="6d435-105">Cuando un usuario interactivo inicia sesión, el sistema asocia la estación de ventana interactiva con la sesión de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="6d435-105">When an interactive user logs on, the system associates the interactive window station with the user logon session.</span></span> <span data-ttu-id="6d435-106">El sistema también crea el escritorio de entrada predeterminado para la estación de ventana interactiva ( \\ valor predeterminado de Winsta0).</span><span class="sxs-lookup"><span data-stu-id="6d435-106">The system also creates the default input desktop for the interactive window station (Winsta0\\default).</span></span> <span data-ttu-id="6d435-107">Los procesos iniciados por el usuario que ha iniciado sesión están asociados al \\ escritorio predeterminado de Winsta0.</span><span class="sxs-lookup"><span data-stu-id="6d435-107">Processes started by the logged-on user are associated with the Winsta0\\default desktop.</span></span>

<span data-ttu-id="6d435-108">Un proceso puede usar la función [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) para crear una nueva estación de ventana y la función **CreateDesktop** o [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) para crear un nuevo escritorio.</span><span class="sxs-lookup"><span data-stu-id="6d435-108">A process can use the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function to create a new window station, and the **CreateDesktop** or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function to create a new desktop.</span></span> <span data-ttu-id="6d435-109">El número de escritorios que se pueden crear está limitado por el tamaño del montón de escritorio del sistema.</span><span class="sxs-lookup"><span data-stu-id="6d435-109">The number of desktops that can be created is limited by the size of the system desktop heap.</span></span> <span data-ttu-id="6d435-110">Para obtener más información, vea [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span><span class="sxs-lookup"><span data-stu-id="6d435-110">For more information, see [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span>

<span data-ttu-id="6d435-111">Cuando un proceso no interactivo, como una aplicación de servicio intenta conectarse a una estación de ventana y no existe ninguna estación de ventana para la sesión de inicio de sesión de proceso, el sistema intenta crear una estación de ventana y un escritorio para la sesión.</span><span class="sxs-lookup"><span data-stu-id="6d435-111">When a noninteractive process such as a service application attempts to connect to a window station and no window station exists for the process logon session, the system attempts to create a window station and desktop for the session.</span></span> <span data-ttu-id="6d435-112">El nombre de la estación de ventana creada se basa en el identificador de la sesión de inicio de sesión y el nombre del escritorio es default, tal como se describe aquí:</span><span class="sxs-lookup"><span data-stu-id="6d435-112">The name of the created window station is based on the logon session identifier, and the desktop is named default, as described here:</span></span>

-   <span data-ttu-id="6d435-113">Si un servicio se ejecuta en el contexto de seguridad de la cuenta LocalSystem pero no incluye el \_ atributo de proceso interactivo de servicio \_ , usa la estación de ventana y el escritorio siguientes: Service-0X0-3e7 $ \\ default.</span><span class="sxs-lookup"><span data-stu-id="6d435-113">If a service is running in the security context of the LocalSystem account but does not include the SERVICE\_INTERACTIVE\_PROCESS attribute, it uses the following window station and desktop: Service-0x0-3e7$\\default.</span></span> <span data-ttu-id="6d435-114">Esta estación de ventana no es interactiva, por lo que el servicio no puede mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6d435-114">This window station is not interactive, so the service cannot display a user interface.</span></span> <span data-ttu-id="6d435-115">Además, los procesos creados por el servicio no pueden mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6d435-115">In addition, processes created by the service cannot display a user interface.</span></span>
-   <span data-ttu-id="6d435-116">Si el servicio se ejecuta en el contexto de seguridad de una cuenta de usuario, el nombre de la estación de ventana se basa en el SID de usuario Service-0x *Z1* - *Z2*$, donde *Z1* es la parte alta del SID de inicio de sesión y *Z2* es la parte baja del SID de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="6d435-116">If the service is running in the security context of a user account, the name of the window station is based on the user SID Service-0x *Z1*-*Z2*$, where *Z1* is the high part of the logon SID and *Z2* is the low part of the logon SID.</span></span> <span data-ttu-id="6d435-117">Dado que un SID es único para la sesión de inicio de sesión, dos servicios que se ejecutan en el mismo contexto de seguridad reciben estaciones de ventana únicas.</span><span class="sxs-lookup"><span data-stu-id="6d435-117">Because a SID is unique to the logon session, two services running in the same security context receive unique window stations.</span></span> <span data-ttu-id="6d435-118">Estas estaciones de ventana no son interactivas.</span><span class="sxs-lookup"><span data-stu-id="6d435-118">These window stations are not interactive.</span></span>

<span data-ttu-id="6d435-119">La lista de control de acceso discrecional (DACL) de la estación de ventana y el escritorio incluyen los siguientes derechos de acceso para la cuenta de usuario del servicio:</span><span class="sxs-lookup"><span data-stu-id="6d435-119">The discretionary access control list (DACL) for the window station and desktop includes the following access rights for the service's user account:</span></span>

<span data-ttu-id="6d435-120">Estación de ventana:</span><span class="sxs-lookup"><span data-stu-id="6d435-120">Window Station:</span></span>

<dl> <span data-ttu-id="6d435-121">WINSTA \_ ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="6d435-121">WINSTA\_ACCESSCLIPBOARD</span></span>  
<span data-ttu-id="6d435-122">WINSTA \_ ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="6d435-122">WINSTA\_ACCESSGLOBALATOMS</span></span>  
<span data-ttu-id="6d435-123">WINSTA \_ CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="6d435-123">WINSTA\_CREATEDESKTOP</span></span>  
<span data-ttu-id="6d435-124">WINSTA \_ EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="6d435-124">WINSTA\_EXITWINDOWS</span></span>  
<span data-ttu-id="6d435-125">WINSTA \_ READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="6d435-125">WINSTA\_READATTRIBUTES</span></span>  
<span data-ttu-id="6d435-126">\_derechos estándar \_ requeridos</span><span class="sxs-lookup"><span data-stu-id="6d435-126">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

<span data-ttu-id="6d435-127">Escritorio:</span><span class="sxs-lookup"><span data-stu-id="6d435-127">Desktop:</span></span>

<dl> <span data-ttu-id="6d435-128">ESCRITORIO \_ CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="6d435-128">DESKTOP\_CREATEMENU</span></span>  
<span data-ttu-id="6d435-129">CREATEWINDOW de escritorio \_</span><span class="sxs-lookup"><span data-stu-id="6d435-129">DESKTOP\_CREATEWINDOW</span></span>  
<span data-ttu-id="6d435-130">\_enumerar escritorio</span><span class="sxs-lookup"><span data-stu-id="6d435-130">DESKTOP\_ENUMERATE</span></span>  
<span data-ttu-id="6d435-131">ESCRITORIO \_ HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="6d435-131">DESKTOP\_HOOKCONTROL</span></span>  
<span data-ttu-id="6d435-132">ESCRITORIO \_ READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6d435-132">DESKTOP\_READOBJECTS</span></span>  
<span data-ttu-id="6d435-133">ESCRITORIO \_ WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="6d435-133">DESKTOP\_WRITEOBJECTS</span></span>  
<span data-ttu-id="6d435-134">\_derechos estándar \_ requeridos</span><span class="sxs-lookup"><span data-stu-id="6d435-134">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

 

 