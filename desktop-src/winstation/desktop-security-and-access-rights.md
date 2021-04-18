---
title: Seguridad de escritorio y derechos de acceso
description: La seguridad le permite controlar el acceso a los objetos de escritorio. Para obtener más información sobre la seguridad, vea modelo de Access-Control.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d18b48e0b80dc39ea1b3f65a77acb615c4cb8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421036"
---
# <a name="desktop-security-and-access-rights"></a><span data-ttu-id="c2c84-104">Seguridad de escritorio y derechos de acceso</span><span class="sxs-lookup"><span data-stu-id="c2c84-104">Desktop Security and Access Rights</span></span>

<span data-ttu-id="c2c84-105">La seguridad le permite controlar el acceso a los objetos de escritorio.</span><span class="sxs-lookup"><span data-stu-id="c2c84-105">Security enables you to control access to desktop objects.</span></span> <span data-ttu-id="c2c84-106">Para obtener más información sobre la seguridad, vea [modelo de control de acceso](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="c2c84-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="c2c84-107">Puede especificar un [descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptors) para un objeto de escritorio cuando llame a la función [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) o [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) .</span><span class="sxs-lookup"><span data-stu-id="c2c84-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a desktop object when you call the [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function.</span></span> <span data-ttu-id="c2c84-108">Si especifica NULL, el escritorio obtiene un descriptor de seguridad predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c2c84-108">If you specify NULL, the desktop gets a default security descriptor.</span></span> <span data-ttu-id="c2c84-109">Las ACL del descriptor de seguridad predeterminado para un escritorio proceden de su estación de ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="c2c84-109">The ACLs in the default security descriptor for a desktop come from its parent window station.</span></span>

<span data-ttu-id="c2c84-110">Para obtener o establecer el descriptor de seguridad de un objeto de estación de ventana, llame a las funciones [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) y [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="c2c84-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="c2c84-111">Cuando se llama a la función [**openDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) o [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) , el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="c2c84-111">When you call the [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) or [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="c2c84-112">Los derechos de acceso válidos para los objetos de escritorio incluyen los [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights) y algunos derechos de acceso específicos del objeto.</span><span class="sxs-lookup"><span data-stu-id="c2c84-112">The valid access rights for desktop objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="c2c84-113">En la tabla siguiente se enumeran los derechos de acceso estándar utilizados por todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="c2c84-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="c2c84-114">Value</span><span class="sxs-lookup"><span data-stu-id="c2c84-114">Value</span></span>                       | <span data-ttu-id="c2c84-115">Significado</span><span class="sxs-lookup"><span data-stu-id="c2c84-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c84-116">ELIMINAR (0x00010000L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="c2c84-117">Necesario para eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="c2c84-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="c2c84-118">CONTROL de lectura \_ (0x00020000L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="c2c84-119">Necesario para leer la información del descriptor de seguridad del objeto, sin incluir la información en la SACL.</span><span class="sxs-lookup"><span data-stu-id="c2c84-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="c2c84-120">Para leer o escribir la SACL, debe solicitar el derecho de \_ acceso de seguridad del sistema de acceso \_ .</span><span class="sxs-lookup"><span data-stu-id="c2c84-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="c2c84-121">Para obtener más información, consulte [derechos de acceso de SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="c2c84-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="c2c84-122">SINCRONIZAr (0x00100000L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="c2c84-123">No se admite para objetos de escritorio.</span><span class="sxs-lookup"><span data-stu-id="c2c84-123">Not supported for desktop objects.</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c2c84-124">ESCRIBIR \_ DAC (0x00040000L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="c2c84-125">Necesario para modificar la DACL en el descriptor de seguridad para el objeto.</span><span class="sxs-lookup"><span data-stu-id="c2c84-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="c2c84-126">Propietario de escritura \_ (0x00080000L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="c2c84-127">Necesario para cambiar el propietario del descriptor de seguridad para el objeto.</span><span class="sxs-lookup"><span data-stu-id="c2c84-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="c2c84-128">En la tabla siguiente se enumeran los derechos de acceso específicos del objeto.</span><span class="sxs-lookup"><span data-stu-id="c2c84-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="c2c84-129">Derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="c2c84-129">Access right</span></span>                       | <span data-ttu-id="c2c84-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2c84-130">Description</span></span>                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c84-131">DESKTOP \_ CREATEMENU (0x0004L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-131">DESKTOP\_CREATEMENU (0x0004L)</span></span>      | <span data-ttu-id="c2c84-132">Se requiere para crear un menú en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="c2c84-132">Required to create a menu on the desktop.</span></span>                                                   |
| <span data-ttu-id="c2c84-133">CREATEWINDOW de escritorio \_ (0x0002L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-133">DESKTOP\_CREATEWINDOW (0x0002L)</span></span>    | <span data-ttu-id="c2c84-134">Se requiere para crear una ventana en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="c2c84-134">Required to create a window on the desktop.</span></span>                                                 |
| <span data-ttu-id="c2c84-135">\_Enumeración de escritorio (0x0040L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-135">DESKTOP\_ENUMERATE (0x0040L)</span></span>       | <span data-ttu-id="c2c84-136">Necesario para que se enumere el escritorio.</span><span class="sxs-lookup"><span data-stu-id="c2c84-136">Required for the desktop to be enumerated.</span></span>                                                  |
| <span data-ttu-id="c2c84-137">DESKTOP \_ HOOKCONTROL (0x0008L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-137">DESKTOP\_HOOKCONTROL (0x0008L)</span></span>     | <span data-ttu-id="c2c84-138">Necesario para establecer cualquiera de los enlaces de ventana.</span><span class="sxs-lookup"><span data-stu-id="c2c84-138">Required to establish any of the window hooks.</span></span>                                              |
| <span data-ttu-id="c2c84-139">DESKTOP \_ JOURNALPLAYBACK (0x0020L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-139">DESKTOP\_JOURNALPLAYBACK (0x0020L)</span></span> | <span data-ttu-id="c2c84-140">Necesario para realizar la reproducción del diario en un escritorio.</span><span class="sxs-lookup"><span data-stu-id="c2c84-140">Required to perform journal playback on a desktop.</span></span>                                          |
| <span data-ttu-id="c2c84-141">DESKTOP \_ JOURNALRECORD (0x0010L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-141">DESKTOP\_JOURNALRECORD (0x0010L)</span></span>   | <span data-ttu-id="c2c84-142">Necesario para realizar la grabación del diario en un escritorio.</span><span class="sxs-lookup"><span data-stu-id="c2c84-142">Required to perform journal recording on a desktop.</span></span>                                         |
| <span data-ttu-id="c2c84-143">DESKTOP \_ READOBJECTS (0x0001L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-143">DESKTOP\_READOBJECTS (0x0001L)</span></span>     | <span data-ttu-id="c2c84-144">Necesario para leer objetos en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="c2c84-144">Required to read objects on the desktop.</span></span>                                                    |
| <span data-ttu-id="c2c84-145">DESKTOP \_ SWITCHDESKTOP (0x0100L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-145">DESKTOP\_SWITCHDESKTOP (0x0100L)</span></span>   | <span data-ttu-id="c2c84-146">Necesario para activar el escritorio mediante la función [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) .</span><span class="sxs-lookup"><span data-stu-id="c2c84-146">Required to activate the desktop using the [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) function.</span></span> |
| <span data-ttu-id="c2c84-147">DESKTOP \_ WRITEOBJECTS (0x0080L)</span><span class="sxs-lookup"><span data-stu-id="c2c84-147">DESKTOP\_WRITEOBJECTS (0x0080L)</span></span>    | <span data-ttu-id="c2c84-148">Se requiere para escribir objetos en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="c2c84-148">Required to write objects on the desktop.</span></span>                                                   |



 

<span data-ttu-id="c2c84-149">A continuación se muestran los [derechos de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para un objeto de escritorio incluido en la estación de ventana interactiva de la sesión de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="c2c84-149">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a desktop object contained in the interactive window station of the user's logon session.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c2c84-150">Derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="c2c84-150">Access right</span></span></th>
<th><span data-ttu-id="c2c84-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2c84-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2c84-152">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="c2c84-152">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="c2c84-153">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="c2c84-153">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="c2c84-154">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c2c84-154">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="c2c84-155">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="c2c84-155">STANDARD_RIGHTS_READ</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2c84-156">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="c2c84-156">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="c2c84-157">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="c2c84-157">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="c2c84-158">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="c2c84-158">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="c2c84-159">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="c2c84-159">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="c2c84-160">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="c2c84-160">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="c2c84-161">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="c2c84-161">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="c2c84-162">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c2c84-162">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="c2c84-163">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="c2c84-163">STANDARD_RIGHTS_WRITE</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2c84-164">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="c2c84-164">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="c2c84-165">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="c2c84-165">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="c2c84-166">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="c2c84-166">STANDARD_RIGHTS_EXECUTE</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2c84-167">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="c2c84-167">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="c2c84-168">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="c2c84-168">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="c2c84-169">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="c2c84-169">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="c2c84-170">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="c2c84-170">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="c2c84-171">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="c2c84-171">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="c2c84-172">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="c2c84-172">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="c2c84-173">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="c2c84-173">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="c2c84-174">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c2c84-174">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="c2c84-175">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="c2c84-175">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="c2c84-176">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="c2c84-176">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="c2c84-177">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="c2c84-177">STANDARD_RIGHTS_REQUIRED</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c2c84-178">Puede solicitar el derecho de \_ acceso de seguridad del sistema de acceso \_ a un objeto de escritorio si desea leer o escribir la SACL del objeto.</span><span class="sxs-lookup"><span data-stu-id="c2c84-178">You can request the ACCESS\_SYSTEM\_SECURITY access right to a desktop object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="c2c84-179">Para obtener más información, consulte derechos [de acceso de las listas de control de acceso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) y [SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="c2c84-179">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 