---
title: Proporcionar permisos de usuario para dispositivos de grabación de multimedia
description: De forma predeterminada, tanto Windows Vista como Windows Server 2008 conceden acceso de lectura y escritura a los administradores y usuarios registrados directamente en el equipo (usuarios intermedios).
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613eb1bba9a18cfb08e1eee3e6b86c34235ab8e9
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104279725"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a><span data-ttu-id="bce5d-103">Proporcionar permisos de usuario para dispositivos de grabación de multimedia</span><span class="sxs-lookup"><span data-stu-id="bce5d-103">Providing User Permissions for Media Burning Devices</span></span>

<span data-ttu-id="bce5d-104">De forma predeterminada, tanto Windows Vista como Windows Server 2008 conceden acceso de lectura y escritura a los administradores y usuarios registrados directamente en el equipo (usuarios intermedios).</span><span class="sxs-lookup"><span data-stu-id="bce5d-104">By default, both Windows Vista and Windows Server 2008 grant read/write access to administrators and users logged directly into the machine (intermediate users).</span></span> <span data-ttu-id="bce5d-105">Sin embargo, en Windows XP y Windows Server 2003, un administrador debe conceder a estos dispositivos privilegios de lectura y escritura para otros grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="bce5d-105">However, in Windows XP and Windows Server 2003 an administrator must grant these device read/write privileges to other user groups.</span></span>

<span data-ttu-id="bce5d-106">Un administrador puede ajustar permisos específicos del dispositivo para usuarios avanzados y usuarios interactivos.</span><span class="sxs-lookup"><span data-stu-id="bce5d-106">An administrator may adjust specific device-related permissions for power users and interactive users.</span></span>

<span data-ttu-id="bce5d-107">Para llegar al panel de permisos de grupo adecuado en Windows XP, haga clic en **Inicio**, haga clic en **Ejecutar**, escriba **gpedit. msc** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="bce5d-107">To reach the appropriate group permissions panel in Windows XP, click **Start**, click **Run**, type **gpedit.msc**, and then click **OK**.</span></span> <span data-ttu-id="bce5d-108">En la interfaz de directiva de grupo, expanda **configuración del equipo**, **configuración de Windows**, **configuración de seguridad**, **Directivas locales** y, a continuación, haga doble clic en **Opciones de seguridad**.</span><span class="sxs-lookup"><span data-stu-id="bce5d-108">In the Group Policy interface, expand **Computer Configuration**, expand **Windows Settings**, expand **Security Settings**, expand **Local Policies**, and double-click **Security Options**.</span></span>

![Captura de pantalla que muestra la ventana ' directiva de grupo ' con una directiva seleccionada en el panel ' Directiva '.](images/gpolpanel.jpg)

<span data-ttu-id="bce5d-110">En este panel, el administrador debe especificar la configuración de dos opciones de dispositivo para proporcionar los permisos de grupo necesarios:</span><span class="sxs-lookup"><span data-stu-id="bce5d-110">At this panel, an administrator must specify the settings of two device options to provide the required group permissions:</span></span>

-   <span data-ttu-id="bce5d-111">Establecer "dispositivos: restringir el acceso a CD-ROM solo al usuario con sesión iniciada localmente" en **habilitado**</span><span class="sxs-lookup"><span data-stu-id="bce5d-111">Set "Devices: Restrict CD-ROM access to locally logged-on user only" to **Enabled**</span></span>
-   <span data-ttu-id="bce5d-112">Establezca "dispositivos: permitidos para formatear y expulsar medios extraíbles" a **administradores y usuarios avanzados**.</span><span class="sxs-lookup"><span data-stu-id="bce5d-112">Set "Devices: Allowed to format and eject removable media" to **Administrators and Power Users**.</span></span> <span data-ttu-id="bce5d-113">También es posible emular los permisos de Windows Vista si se establece esta opción en **administradores y usuarios interactivos**.</span><span class="sxs-lookup"><span data-stu-id="bce5d-113">It is also possible to emulate Windows Vista permissions by setting this option to **Administrators and Interactive Users**.</span></span>

<span data-ttu-id="bce5d-114">Aunque una interfaz de usuario específica no existe en Windows XP o Windows Server 2003 para el uso de [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) o [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), es posible usar estas API para conceder permisos de dispositivo a los grupos de usuarios personalizados.</span><span class="sxs-lookup"><span data-stu-id="bce5d-114">While a specific UI does not exist in Windows XP or Windows Server 2003 for the use of [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) or [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), it is possible to use these APIs to grant custom user groups device permissions.</span></span> <span data-ttu-id="bce5d-115">Por ejemplo, una llamada a **SetSecurityInfo** concederá permisos a los grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="bce5d-115">For example, a call to **SetSecurityInfo** will grant permissions to user groups.</span></span> <span data-ttu-id="bce5d-116">Los cambios de permisos con esta API son temporales y no se conservarán durante un reinicio.</span><span class="sxs-lookup"><span data-stu-id="bce5d-116">Permission changes with this API are temporary and will not persist across a reboot.</span></span> <span data-ttu-id="bce5d-117">Sin embargo, al llamar a [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) se implementarán los cambios de permisos en el registro, que se conservarán en un reinicio.</span><span class="sxs-lookup"><span data-stu-id="bce5d-117">However, calling [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) will implement the permission changes in the registry, which will persist across a reboot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bce5d-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bce5d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bce5d-119">Usar IMAPi</span><span class="sxs-lookup"><span data-stu-id="bce5d-119">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="bce5d-120">**SetSecurityInfo**</span><span class="sxs-lookup"><span data-stu-id="bce5d-120">**SetSecurityInfo**</span></span>](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[<span data-ttu-id="bce5d-121">SetupDiSetDeviceRegistryProperty</span><span class="sxs-lookup"><span data-stu-id="bce5d-121">SetupDiSetDeviceRegistryProperty</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 