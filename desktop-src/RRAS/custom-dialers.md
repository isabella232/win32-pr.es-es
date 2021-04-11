---
title: Marcadores personalizados
description: Los sistemas operativos Windows 2000 y versiones posteriores permiten a los desarrolladores proporcionar sus propios marcadores personalizados que funcionan con el servicio de acceso remoto (RAS).
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Marcadores personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35293de408a2a0faa146b93f9b5d5ebccf447acc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271318"
---
# <a name="custom-dialers"></a><span data-ttu-id="0dfc4-104">Marcadores personalizados</span><span class="sxs-lookup"><span data-stu-id="0dfc4-104">Custom Dialers</span></span>

<span data-ttu-id="0dfc4-105">Los sistemas operativos Windows 2000 y versiones posteriores permiten a los desarrolladores proporcionar sus propios marcadores personalizados que funcionan con el servicio de acceso remoto (RAS).</span><span class="sxs-lookup"><span data-stu-id="0dfc4-105">Windows 2000 and later operating systems enable developers to provide their own custom dialers that work with the Remote Access Service (RAS).</span></span> <span data-ttu-id="0dfc4-106">El marcador personalizado se implementa como una única biblioteca de vínculos dinámicos (DLL) que exporta los siguientes puntos de entrada:</span><span class="sxs-lookup"><span data-stu-id="0dfc4-106">The custom dialer is implemented as a single dynamic-link library (DLL) that exports the following entry points:</span></span>

-   [<span data-ttu-id="0dfc4-107">**RasCustomDial**</span><span class="sxs-lookup"><span data-stu-id="0dfc4-107">**RasCustomDial**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [<span data-ttu-id="0dfc4-108">**RasCustomDialDlg**</span><span class="sxs-lookup"><span data-stu-id="0dfc4-108">**RasCustomDialDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [<span data-ttu-id="0dfc4-109">**RasCustomHangup**</span><span class="sxs-lookup"><span data-stu-id="0dfc4-109">**RasCustomHangup**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [<span data-ttu-id="0dfc4-110">**RasCustomEntryDlg**</span><span class="sxs-lookup"><span data-stu-id="0dfc4-110">**RasCustomEntryDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [<span data-ttu-id="0dfc4-111">**RasCustomDeleteEntryNotify**</span><span class="sxs-lookup"><span data-stu-id="0dfc4-111">**RasCustomDeleteEntryNotify**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

<span data-ttu-id="0dfc4-112">El archivo DLL de marcado personalizado debe exportar todos estos puntos de entrada y debe implementar los puntos de entrada como funciones Unicode.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-112">The custom-dial DLL must export all of these entry points, and it must implement the entry points as Unicode functions.</span></span> <span data-ttu-id="0dfc4-113">Para obtener más información acerca de estas funciones, consulte la página de referencia de cada función en la Windows SDK referencia del servicio de acceso remoto.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-113">For more information about these functions, see the reference page for each function in the Windows SDK Remote Access Service Reference.</span></span>

<span data-ttu-id="0dfc4-114">Para que una conexión RAS use el marcador personalizado, la entrada de la libreta de teléfonos para la conexión debe contener la ruta de acceso al archivo DLL de marcado personalizado.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-114">In order for a RAS connection to use the custom dialer, the phone-book entry for the connection must contain the path to the custom-dial DLL.</span></span> <span data-ttu-id="0dfc4-115">Use las funciones de la API de RAS [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) y [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para establecer esta ruta de acceso en el miembro **szCustomDialDll** de la estructura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) para la entrada de la libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-115">Use the RAS API functions [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) and [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) to set this path in the **szCustomDialDll** member of the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure for the phone-book entry.</span></span>

## <a name="updating-the-registry-for-custom-dialers"></a><span data-ttu-id="0dfc4-116">Actualización del registro de marcadores personalizados</span><span class="sxs-lookup"><span data-stu-id="0dfc4-116">Updating the Registry for Custom Dialers</span></span>

<span data-ttu-id="0dfc4-117">Para que el sistema Marque una conexión que utiliza un marcador personalizado, la ruta de acceso al archivo DLL de marcado personalizado debe existir en el siguiente valor del registro.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-117">In order for the system to dial a connection that uses a custom dialer, the path to the custom-dial DLL must exist in the following registry value.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
                  CustomDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

<span data-ttu-id="0dfc4-118">Dado que **CustomDLL** es de tipo **reg \_ multi \_ SZ**, puede contener rutas de acceso a varios archivos dll de marcado personalizado.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-118">Because **CustomDLL** is of type **REG\_MULTI\_SZ**, it can hold paths to multiple custom-dial DLLs.</span></span> <span data-ttu-id="0dfc4-119">Debe establecer la ruta de acceso a la DLL de marcado personalizado en este valor del registro, además de la entrada de la libreta de teléfonos de la conexión.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-119">You need to set the path to the custom-dial DLL in this registry value, in addition to the phone-book entry for the connection.</span></span>

<span data-ttu-id="0dfc4-120">De forma predeterminada, este valor del registro solo lo pueden escribir los usuarios con privilegios de administrador o sistema.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-120">By default, this registry value is writeable only by a user with Administrator or System privileges.</span></span> <span data-ttu-id="0dfc4-121">Por motivos de seguridad, no cambie los permisos de esta clave del registro.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-121">For security reasons, do not change the permissions on this registry key.</span></span>

## <a name="using-custom-dialers-at-system-logon"></a><span data-ttu-id="0dfc4-122">Uso de marcadores personalizados al iniciar sesión en el sistema</span><span class="sxs-lookup"><span data-stu-id="0dfc4-122">Using Custom Dialers at System Logon</span></span>

<span data-ttu-id="0dfc4-123">Los sistemas operativos Windows 2000 y versiones posteriores permiten a un usuario establecer una conexión RAS en el momento del inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-123">Windows 2000 and later operating systems allow a user to establish a RAS connection at the time of logon.</span></span> <span data-ttu-id="0dfc4-124">Para ello, el usuario comprueba el **Inicio de sesión mediante acceso telefónico a redes** en el cuadro de diálogo **información de inicio de sesión** .</span><span class="sxs-lookup"><span data-stu-id="0dfc4-124">To do so, the user checks **Logon using Dial-up Networking** in the **Logon Information** dialog box.</span></span> <span data-ttu-id="0dfc4-125">Cuando el usuario hace clic en el botón Aceptar, el sistema muestra las conexiones disponibles.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-125">After the user clicks the Okay button, the system displays the available connections.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="0dfc4-126">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="0dfc4-126">Security Considerations</span></span>

<span data-ttu-id="0dfc4-127">En la mayoría de los casos, un marcador personalizado funciona con los privilegios de seguridad del usuario que lo invoca.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-127">In most cases, a custom dialer operates with the security privileges of the user that invokes it.</span></span> <span data-ttu-id="0dfc4-128">Sin embargo, si se invoca el marcador personalizado durante el inicio de sesión, funciona con privilegios del sistema.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-128">However, if the custom dialer is invoked at logon, it operates with system privileges.</span></span> <span data-ttu-id="0dfc4-129">Por lo tanto, diseñe el marcador personalizado para que no se pueda usar para infringir la seguridad del sistema.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-129">Therefore, design the custom dialer so that it cannot be used to violate system security.</span></span> <span data-ttu-id="0dfc4-130">Por ejemplo, el marcador no debería presentar una interfaz de usuario que permita al usuario escribir en el sistema de archivos del equipo.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-130">For example, the dialer should not present a user interface that allows the user write access to the computer's file system.</span></span> <span data-ttu-id="0dfc4-131">Entre las interfaces de usuario que proporcionan este tipo de acceso se incluyen el cuadro de diálogo **Buscar archivo** , el cuadro de diálogo común **Abrir archivo** y la **ayuda** de Windows.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-131">User interfaces that provide such access include the **Find-File** dialog, the **File-Open** common dialog, and Windows **Help**.</span></span>

## <a name="custom-dialer-user-interface-must-support-idcancel"></a><span data-ttu-id="0dfc4-132">La interfaz de usuario de marcación personalizada debe ser compatible con IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="0dfc4-132">Custom Dialer User Interface Must Support IDCANCEL</span></span>

<span data-ttu-id="0dfc4-133">Si el marcador personalizado muestra una interfaz de usuario, la interfaz de usuario debe admitir \_ mensajes de comandos de WM en los que LOWORD (*wParam*) es igual a IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="0dfc4-133">If the custom dialer displays a user interface, the user interface must support WM\_COMMAND messages where LOWORD(*wParam*) equals IDCANCEL.</span></span>

 

 