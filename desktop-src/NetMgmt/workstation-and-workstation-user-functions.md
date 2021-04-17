---
title: Funciones de usuario de estación de trabajo y estación de trabajo
description: Las funciones de la estación de trabajo de administración de redes realizan tareas administrativas en una estación de trabajo local o remota.
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd445746bca51abaa0cd72877bdf03dd4d00d338
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665865"
---
# <a name="workstation-and-workstation-user-functions"></a><span data-ttu-id="e7e5a-103">Funciones de usuario de estación de trabajo y estación de trabajo</span><span class="sxs-lookup"><span data-stu-id="e7e5a-103">Workstation and Workstation User Functions</span></span>

<span data-ttu-id="e7e5a-104">Las funciones de la estación de trabajo de administración de redes realizan tareas administrativas en una estación de trabajo local o remota.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-104">The network management workstation functions perform administrative tasks on a local or remote workstation.</span></span> <span data-ttu-id="e7e5a-105">Solo un usuario o aplicación con pertenencia a un grupo de administradores, en un servidor local o remoto, puede realizar tareas administrativas en una estación de trabajo para controlar el funcionamiento, el acceso de usuario y el uso compartido de recursos.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-105">Only a user or application with admin group membership, on a local or remote server, can perform administrative tasks on a workstation to control its operation, user access, and resource sharing.</span></span> <span data-ttu-id="e7e5a-106">Para obtener más información sobre cómo llamar a funciones que requieran privilegios de administrador, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="e7e5a-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="e7e5a-107">A continuación se enumeran las funciones de estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-107">The workstation functions are listed following.</span></span>



| <span data-ttu-id="e7e5a-108">Función</span><span class="sxs-lookup"><span data-stu-id="e7e5a-108">Function</span></span>                                   | <span data-ttu-id="e7e5a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7e5a-109">Description</span></span>                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="e7e5a-110">**NetWkstaGetInfo**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-110">**NetWkstaGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | <span data-ttu-id="e7e5a-111">Devuelve información sobre los elementos de configuración de una estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-111">Returns information about the configuration elements for a workstation.</span></span> |
| [<span data-ttu-id="e7e5a-112">**NetWkstaSetInfo**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-112">**NetWkstaSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | <span data-ttu-id="e7e5a-113">Configura una estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-113">Configures a workstation.</span></span>                                               |



 

<span data-ttu-id="e7e5a-114">Las funciones de estación de trabajo permiten el acceso a dos tipos discretos de información de la estación de trabajo:</span><span class="sxs-lookup"><span data-stu-id="e7e5a-114">The workstation functions allow access to two discrete types of workstation information:</span></span>

-   <span data-ttu-id="e7e5a-115">Información del sistema</span><span class="sxs-lookup"><span data-stu-id="e7e5a-115">System information</span></span>
-   <span data-ttu-id="e7e5a-116">Información específica de la plataforma</span><span class="sxs-lookup"><span data-stu-id="e7e5a-116">Platform-specific information</span></span>

<span data-ttu-id="e7e5a-117">Dentro de cada tipo, los datos se clasifican por acceso de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-117">Within each type the data is categorized by security access.</span></span> <span data-ttu-id="e7e5a-118">Los datos a los que se puede tener acceso como invitados son un subconjunto de los datos a los que puede acceder el usuario, que a su vez es un subconjunto de los datos accesibles desde el administrador.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-118">Data that is guest-accessible is a subset of the data that is user-accessible, which is in turn a subset of the admin-accessible data.</span></span>

<span data-ttu-id="e7e5a-119">La información de la estación de trabajo está disponible en los siguientes niveles:</span><span class="sxs-lookup"><span data-stu-id="e7e5a-119">Workstation information is available at the following levels:</span></span>

-   [<span data-ttu-id="e7e5a-120">**WKSTA \_ INFO \_ 100**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-120">**WKSTA\_INFO\_100**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [<span data-ttu-id="e7e5a-121">**WKSTA \_ INFO \_ 101**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-121">**WKSTA\_INFO\_101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [<span data-ttu-id="e7e5a-122">**WKSTA \_ INFO \_ 102**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-122">**WKSTA\_INFO\_102**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

<span data-ttu-id="e7e5a-123">Las funciones de usuario de la estación de trabajo de administración de red permiten el acceso a información específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-123">The network management workstation user functions allow access to user-specific information.</span></span> <span data-ttu-id="e7e5a-124">La información específica del usuario se separa de la información de la estación de trabajo porque puede haber más de un usuario en una estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-124">The user-specific information is separated from the workstation information because there can be more than one user on a workstation.</span></span>

<span data-ttu-id="e7e5a-125">A continuación se enumeran las funciones de usuario de la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-125">The workstation user functions are listed following.</span></span>



| <span data-ttu-id="e7e5a-126">Función</span><span class="sxs-lookup"><span data-stu-id="e7e5a-126">Function</span></span>                                           | <span data-ttu-id="e7e5a-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7e5a-127">Description</span></span>                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7e5a-128">**NetWkstaUserEnum**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-128">**NetWkstaUserEnum**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | <span data-ttu-id="e7e5a-129">Muestra información acerca de todos los usuarios que han iniciado sesión actualmente en la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-129">Lists information about all users currently logged on to the workstation.</span></span>           |
| [<span data-ttu-id="e7e5a-130">**NetWkstaUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-130">**NetWkstaUserGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | <span data-ttu-id="e7e5a-131">Devuelve información acerca de un usuario que ha iniciado sesión actualmente.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-131">Returns information about one currently logged-on user.</span></span>                             |
| [<span data-ttu-id="e7e5a-132">**NetWkstaUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-132">**NetWkstaUserSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | <span data-ttu-id="e7e5a-133">Establece la información específica del usuario para los elementos de configuración de una estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-133">Sets the user-specific information for the configuration elements of a workstation.</span></span> |



 

<span data-ttu-id="e7e5a-134">La información de usuario de la estación de trabajo está disponible en los siguientes niveles:</span><span class="sxs-lookup"><span data-stu-id="e7e5a-134">Workstation user information is available at the following levels:</span></span>

-   [<span data-ttu-id="e7e5a-135">**Información de usuario de WKSTA \_ \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-135">**WKSTA\_USER\_INFO\_0**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [<span data-ttu-id="e7e5a-136">**Información de usuario de WKSTA \_ \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-136">**WKSTA\_USER\_INFO\_1**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [<span data-ttu-id="e7e5a-137">**Información de usuario de WKSTA \_ \_ \_ 1101**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-137">**WKSTA\_USER\_INFO\_1101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 