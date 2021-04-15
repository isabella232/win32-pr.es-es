---
title: Acerca de la administración del servicio de acceso remoto
description: Los sistemas operativos Windows 2000 y versiones posteriores proporcionan un conjunto de funciones para administrar los permisos y puertos de usuario en los servidores RAS.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- RRAS del servicio de enrutamiento y acceso remoto, administración de RAS
- RRAS del servicio de enrutamiento y acceso remoto, administración de RAS, descripción
- RRAS de administración de RAS
- RRAS de administración de RAS, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bdb55049e99b6d3df9980fc35879341b488531
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676173"
---
# <a name="about-remote-access-service-administration"></a><span data-ttu-id="db3c1-107">Acerca de la administración del servicio de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="db3c1-107">About Remote Access Service Administration</span></span>

<span data-ttu-id="db3c1-108">Los sistemas operativos Windows 2000 y versiones posteriores proporcionan un conjunto de funciones para administrar los permisos y puertos de usuario en los servidores RAS.</span><span class="sxs-lookup"><span data-stu-id="db3c1-108">Windows 2000 and later operating systems provide a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="db3c1-109">Con estas funciones, puede desarrollar una aplicación de administración del servidor RAS para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="db3c1-109">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="db3c1-110">Enumerar a los usuarios que tienen un conjunto especificado de permisos de RAS</span><span class="sxs-lookup"><span data-stu-id="db3c1-110">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="db3c1-111">Asignar o revocar permisos RAS para un usuario especificado</span><span class="sxs-lookup"><span data-stu-id="db3c1-111">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="db3c1-112">Enumerar los puertos configurados en un servidor RAS</span><span class="sxs-lookup"><span data-stu-id="db3c1-112">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="db3c1-113">Obtener información y estadísticas acerca de un puerto específico en un servidor RAS</span><span class="sxs-lookup"><span data-stu-id="db3c1-113">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="db3c1-114">Restablecer los contadores de estadísticas de un puerto específico</span><span class="sxs-lookup"><span data-stu-id="db3c1-114">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="db3c1-115">Desconectar un puerto especificado</span><span class="sxs-lookup"><span data-stu-id="db3c1-115">Disconnect a specified port</span></span>

<span data-ttu-id="db3c1-116">También puede instalar un archivo DLL de administración del servidor RAS para auditar las conexiones de usuario y asignar direcciones IP a los usuarios de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="db3c1-116">You can also install a RAS server administration DLL to audit user connections and assign IP addresses to dial-in users.</span></span> <span data-ttu-id="db3c1-117">El archivo DLL exporta un conjunto de funciones a las que el servidor RAS llama cuando un usuario intenta conectarse o desconectarse.</span><span class="sxs-lookup"><span data-stu-id="db3c1-117">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

<span data-ttu-id="db3c1-118">En esta documentación se describen los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="db3c1-118">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="db3c1-119">Comparación de funciones: Windows 2000 frente a RRAS Redistributable</span><span class="sxs-lookup"><span data-stu-id="db3c1-119">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [<span data-ttu-id="db3c1-120">Administración de usuarios de RAS</span><span class="sxs-lookup"><span data-stu-id="db3c1-120">RAS User Administration</span></span>](ras-user-administration.md)
-   [<span data-ttu-id="db3c1-121">Administración de puertos y servidores RAS</span><span class="sxs-lookup"><span data-stu-id="db3c1-121">RAS Server and Port Administration</span></span>](ras-server-and-port-administration.md)
-   [<span data-ttu-id="db3c1-122">DLL de administración de RAS</span><span class="sxs-lookup"><span data-stu-id="db3c1-122">RAS Administration DLL</span></span>](ras-administration-dll.md)
-   [<span data-ttu-id="db3c1-123">Configuración del registro del archivo DLL de administración de RAS</span><span class="sxs-lookup"><span data-stu-id="db3c1-123">RAS Administration DLL Registry Setup</span></span>](ras-administration-dll-registry-setup.md)

 

 




