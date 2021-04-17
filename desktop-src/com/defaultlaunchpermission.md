---
title: DefaultLaunchPermission
description: Define la lista de Access Control (ACL) de las entidades de seguridad que pueden iniciar clases que no especifican su propia ACL a través del valor del registro LaunchPermission.
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- Valor del registro DefaultLaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599a0993a4a1238e57e357f428f7046331412cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704817"
---
# <a name="defaultlaunchpermission"></a><span data-ttu-id="29d40-104">DefaultLaunchPermission</span><span class="sxs-lookup"><span data-stu-id="29d40-104">DefaultLaunchPermission</span></span>

<span data-ttu-id="29d40-105">Define la lista de Access Control (ACL) de las entidades de seguridad que pueden iniciar clases que no especifican su propia ACL a través del valor del registro [**LaunchPermission**](launchpermission.md) .</span><span class="sxs-lookup"><span data-stu-id="29d40-105">Defines the Access Control List (ACL) of the principals that can launch classes that do not specify their own ACL through the [**LaunchPermission**](launchpermission.md) registry value.</span></span>

> [!Caution]  
> <span data-ttu-id="29d40-106">No se recomienda cambiar este valor, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="29d40-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="29d40-107">Si va a cambiar este valor para que afecte a la configuración de seguridad de una aplicación COM determinada, debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM en particular.</span><span class="sxs-lookup"><span data-stu-id="29d40-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="29d40-108">Para obtener más información sobre cómo establecer la seguridad de todo el proceso, consulte [configuración de la seguridad de todo el proceso](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="29d40-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="29d40-109">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="29d40-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="29d40-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29d40-110">Remarks</span></span>

<span data-ttu-id="29d40-111">Se trata de un valor **\_ binario de registro** .</span><span class="sxs-lookup"><span data-stu-id="29d40-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="29d40-112">Los permisos de acceso predeterminados son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="29d40-112">The default access permissions are as follows:</span></span>

-   <span data-ttu-id="29d40-113">Administradores: permitir el inicio</span><span class="sxs-lookup"><span data-stu-id="29d40-113">Administrators: allow launch</span></span>
-   <span data-ttu-id="29d40-114">SISTEMA: permitir el inicio</span><span class="sxs-lookup"><span data-stu-id="29d40-114">SYSTEM: allow launch</span></span>
-   <span data-ttu-id="29d40-115">INTERACTIVO: permitir el inicio</span><span class="sxs-lookup"><span data-stu-id="29d40-115">INTERACTIVE: allow launch</span></span>

<span data-ttu-id="29d40-116">Si el valor [**LaunchPermission**](launchpermission.md) se establece para un servidor, tiene prioridad sobre el valor **DefaultLaunchPermission** .</span><span class="sxs-lookup"><span data-stu-id="29d40-116">If the [**LaunchPermission**](launchpermission.md) value is set for a server, it takes precedence over the **DefaultLaunchPermission** value.</span></span> <span data-ttu-id="29d40-117">Al recibir una solicitud local o remota para iniciar un servidor cuya clave [**AppID**](appid-key.md) no tiene su propio valor de **LAUNCHPERMISSION** , la ACL descrita por este valor se comprueba durante la suplantación del cliente y su éxito permite o impide el inicio del código de clase.</span><span class="sxs-lookup"><span data-stu-id="29d40-117">Upon receiving a local or remote request to launch a server whose [**AppID**](appid-key.md) key has no **LaunchPermission** value of its own, the ACL described by this value is checked while impersonating the client and its success either allows or disallows the launching of the class code.</span></span>

<span data-ttu-id="29d40-118">Este valor proporciona un nivel simple de administración centralizada del acceso de inicio predeterminado a las clases no administradas de otro modo en un equipo.</span><span class="sxs-lookup"><span data-stu-id="29d40-118">This value provides a simple level of centralized administration of the default launching access to otherwise unadministered classes on a computer.</span></span> <span data-ttu-id="29d40-119">Por ejemplo, un administrador puede usar la herramienta DCOMCNFG para configurar el sistema de modo que permita el acceso de solo lectura a los usuarios avanzados.</span><span class="sxs-lookup"><span data-stu-id="29d40-119">For example, an administrator might use the DCOMCNFG tool to configure the system to allow read-only access for Power Users.</span></span> <span data-ttu-id="29d40-120">Por lo tanto, OLE restringiría las solicitudes de inicio de código de clase a los miembros del grupo usuarios avanzados.</span><span class="sxs-lookup"><span data-stu-id="29d40-120">OLE would therefore restrict requests to launch class code to members of the Power Users group.</span></span> <span data-ttu-id="29d40-121">Después, un administrador puede configurar los permisos de inicio de clases individuales para conceder la capacidad de iniciar código de clase para otros grupos o usuarios individuales según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="29d40-121">An administrator could subsequently configure launch permissions for individual classes to grant the ability to launch class code to other groups or individual users as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29d40-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29d40-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29d40-123">**LaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="29d40-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="29d40-124">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="29d40-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="29d40-125">Establecer la seguridad de todo el proceso</span><span class="sxs-lookup"><span data-stu-id="29d40-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




