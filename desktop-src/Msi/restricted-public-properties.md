---
description: En algunos casos, un usuario que no es administrador del sistema solo puede reemplazar una lista aprobada de propiedades públicas de Windows Installer restringidas.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Propiedades públicas restringidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f08be7f625cd45cdb48373eb0107ade708949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652919"
---
# <a name="restricted-public-properties"></a><span data-ttu-id="50879-103">Propiedades públicas restringidas</span><span class="sxs-lookup"><span data-stu-id="50879-103">Restricted Public Properties</span></span>

<span data-ttu-id="50879-104">En el caso de una instalación administrada, es posible que el autor del paquete tenga que limitar las [propiedades públicas](public-properties.md) que se pasan al lado servidor y que un usuario que no es administrador del sistema puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="50879-104">In the case of a managed installation, the package author may need to limit which [public properties](public-properties.md) are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="50879-105">Normalmente, algunas restricciones son necesarias para mantener un entorno seguro cuando la instalación requiere que el instalador use privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="50879-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span> <span data-ttu-id="50879-106">Si se cumplen todas las condiciones siguientes, un usuario que no sea administrador del sistema solo puede reemplazar una lista aprobada de propiedades públicas restringidas:</span><span class="sxs-lookup"><span data-stu-id="50879-106">If all of the following conditions are met, a user that is not a system administrator can only override an approved list of restricted public properties:</span></span>

-   <span data-ttu-id="50879-107">El sistema es Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="50879-107">The system is Windows 2000.</span></span>
-   <span data-ttu-id="50879-108">El usuario no es un administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="50879-108">The user is not a system administrator.</span></span>
-   <span data-ttu-id="50879-109">La aplicación o el producto se está instalando con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="50879-109">The application or product is being installed with elevated privileges.</span></span>

<span data-ttu-id="50879-110">Si se cumplen todas las condiciones anteriores, el instalador tiene como valor predeterminado la siguiente lista de propiedades públicas restringidas que cualquier usuario puede cambiar:</span><span class="sxs-lookup"><span data-stu-id="50879-110">If all of the above conditions are true, the installer defaults to the following list of restricted public properties that can be changed by any user:</span></span>

-   [<span data-ttu-id="50879-111">**ACTUAR**</span><span class="sxs-lookup"><span data-stu-id="50879-111">**ACTION**</span></span>](action.md)
-   [<span data-ttu-id="50879-112">**AFTERREBOOT**</span><span class="sxs-lookup"><span data-stu-id="50879-112">**AFTERREBOOT**</span></span>](afterreboot.md)
-   [<span data-ttu-id="50879-113">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="50879-113">**ALLUSERS**</span></span>](allusers.md)
-   [<span data-ttu-id="50879-114">**EXECUTEACTION**</span><span class="sxs-lookup"><span data-stu-id="50879-114">**EXECUTEACTION**</span></span>](executeaction.md)
-   [<span data-ttu-id="50879-115">**EXECUTEMODE**</span><span class="sxs-lookup"><span data-stu-id="50879-115">**EXECUTEMODE**</span></span>](executemode.md)
-   [<span data-ttu-id="50879-116">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="50879-116">**FILEADDDEFAULT**</span></span>](fileadddefault.md)
-   [<span data-ttu-id="50879-117">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="50879-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="50879-118">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="50879-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="50879-119">**INSTALLLEVEL**</span><span class="sxs-lookup"><span data-stu-id="50879-119">**INSTALLLEVEL**</span></span>](installlevel.md)
-   [<span data-ttu-id="50879-120">**LIMITUI**</span><span class="sxs-lookup"><span data-stu-id="50879-120">**LIMITUI**</span></span>](limitui.md)
-   [<span data-ttu-id="50879-121">**LOGACTION**</span><span class="sxs-lookup"><span data-stu-id="50879-121">**LOGACTION**</span></span>](logaction.md)
-   [<span data-ttu-id="50879-122">**NoCompanyName**</span><span class="sxs-lookup"><span data-stu-id="50879-122">**NOCOMPANYNAME**</span></span>](nocompanyname.md)
-   [<span data-ttu-id="50879-123">**NoUserName**</span><span class="sxs-lookup"><span data-stu-id="50879-123">**NOUSERNAME**</span></span>](nousername.md)
-   [<span data-ttu-id="50879-124">**MSIENFORCEUPGRADECOMPONENTRULES**</span><span class="sxs-lookup"><span data-stu-id="50879-124">**MSIENFORCEUPGRADECOMPONENTRULES**</span></span>](msienforceupgradecomponentrules.md)
-   [<span data-ttu-id="50879-125">**MSIINSTANCEGUID**</span><span class="sxs-lookup"><span data-stu-id="50879-125">**MSIINSTANCEGUID**</span></span>](msiinstanceguid.md)
-   [<span data-ttu-id="50879-126">**MSINEWINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="50879-126">**MSINEWINSTANCE**</span></span>](msinewinstance.md)
-   [<span data-ttu-id="50879-127">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="50879-127">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
-   [<span data-ttu-id="50879-128">**DISTRIBUCIÓN**</span><span class="sxs-lookup"><span data-stu-id="50879-128">**PATCH**</span></span>](patch.md)
-   [<span data-ttu-id="50879-129">**PRIMARYFOLDER**</span><span class="sxs-lookup"><span data-stu-id="50879-129">**PRIMARYFOLDER**</span></span>](primaryfolder.md)
-   [<span data-ttu-id="50879-130">**PROMPTROLLBACKCOST**</span><span class="sxs-lookup"><span data-stu-id="50879-130">**PROMPTROLLBACKCOST**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="50879-131">**REINICIO**</span><span class="sxs-lookup"><span data-stu-id="50879-131">**REBOOT**</span></span>](reboot.md)
-   [<span data-ttu-id="50879-132">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="50879-132">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="50879-133">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="50879-133">**REINSTALLMODE**</span></span>](reinstallmode.md)
-   [<span data-ttu-id="50879-134">**RECUPER**</span><span class="sxs-lookup"><span data-stu-id="50879-134">**RESUME**</span></span>](resume.md)
-   [<span data-ttu-id="50879-135">**SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="50879-135">**SEQUENCE**</span></span>](sequence.md)
-   [<span data-ttu-id="50879-136">**SHORTFILENAMES**</span><span class="sxs-lookup"><span data-stu-id="50879-136">**SHORTFILENAMES**</span></span>](shortfilenames.md)
-   [<span data-ttu-id="50879-137">**TRANSFORMA**</span><span class="sxs-lookup"><span data-stu-id="50879-137">**TRANSFORMS**</span></span>](transforms.md)
-   [<span data-ttu-id="50879-138">**TRANSFORMSATSOURCE**</span><span class="sxs-lookup"><span data-stu-id="50879-138">**TRANSFORMSATSOURCE**</span></span>](transformsatsource.md)

<span data-ttu-id="50879-139">El autor de un paquete de instalación puede extender esta lista predeterminada para incluir propiedades públicas adicionales mediante la propiedad [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="50879-139">The author of an installation package can extend this default list to include additional public properties by using the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="50879-140">Al establecer la propiedad [**EnableUserControl**](-enableusercontrol.md) o la [Directiva del sistema](system-policy.md) [EnableUserControl](enableusercontrol.md), la lista se amplía a todas las propiedades públicas.</span><span class="sxs-lookup"><span data-stu-id="50879-140">Setting the [**EnableUserControl**](-enableusercontrol.md) property or the [EnableUserControl](enableusercontrol.md)[system policy](system-policy.md) extends the list to all public properties.</span></span> <span data-ttu-id="50879-141">A continuación, todos los usuarios pueden cambiar cualquier propiedad pública.</span><span class="sxs-lookup"><span data-stu-id="50879-141">All users can then change any public property.</span></span>

<span data-ttu-id="50879-142">El instalador establece la propiedad [**RestrictedUserControl**](restrictedusercontrol.md) cada vez que se restringe la lista de propiedades públicas que los usuarios que no son administradores pasan al servidor.</span><span class="sxs-lookup"><span data-stu-id="50879-142">The installer sets the [**RestrictedUserControl**](restrictedusercontrol.md) property whenever the list of public properties passed to the server by non-administrator users is restricted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50879-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50879-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50879-144">Acerca de las propiedades</span><span class="sxs-lookup"><span data-stu-id="50879-144">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



