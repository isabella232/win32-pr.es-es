---
title: Seguridad y derechos de acceso de la estación de ventana
description: La seguridad le permite controlar el acceso a los objetos de la estación de ventana. Para obtener más información sobre la seguridad, vea modelo de Access-Control.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714385"
---
# <a name="window-station-security-and-access-rights"></a><span data-ttu-id="0925d-104">Seguridad y derechos de acceso de la estación de ventana</span><span class="sxs-lookup"><span data-stu-id="0925d-104">Window Station Security and Access Rights</span></span>

<span data-ttu-id="0925d-105">La seguridad le permite controlar el acceso a los objetos de la estación de ventana.</span><span class="sxs-lookup"><span data-stu-id="0925d-105">Security enables you to control access to window station objects.</span></span> <span data-ttu-id="0925d-106">Para obtener más información sobre la seguridad, vea [modelo de control de acceso](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="0925d-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="0925d-107">Puede especificar un [descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptors) para un objeto de estación de ventana cuando llame a la función [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) .</span><span class="sxs-lookup"><span data-stu-id="0925d-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a window station object when you call the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function.</span></span> <span data-ttu-id="0925d-108">Si especifica NULL, la estación de ventana obtiene un descriptor de seguridad predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0925d-108">If you specify NULL, the window station gets a default security descriptor.</span></span> <span data-ttu-id="0925d-109">Las ACL del descriptor de seguridad predeterminado de una estación de ventana proceden del token principal o de suplantación del creador.</span><span class="sxs-lookup"><span data-stu-id="0925d-109">The ACLs in the default security descriptor for a window station come from the primary or impersonation token of the creator.</span></span>

<span data-ttu-id="0925d-110">Para obtener o establecer el descriptor de seguridad de un objeto de estación de ventana, llame a las funciones [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) y [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="0925d-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="0925d-111">Cuando se llama a la función [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) , el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="0925d-111">When you call the [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="0925d-112">Los derechos de acceso válidos para los objetos de la estación de ventana incluyen los [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights) y algunos derechos de acceso específicos del objeto.</span><span class="sxs-lookup"><span data-stu-id="0925d-112">The valid access rights for window station objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="0925d-113">En la tabla siguiente se enumeran los derechos de acceso estándar utilizados por todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="0925d-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="0925d-114">Value</span><span class="sxs-lookup"><span data-stu-id="0925d-114">Value</span></span>                       | <span data-ttu-id="0925d-115">Significado</span><span class="sxs-lookup"><span data-stu-id="0925d-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0925d-116">ELIMINAR (0x00010000L)</span><span class="sxs-lookup"><span data-stu-id="0925d-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="0925d-117">Necesario para eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="0925d-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="0925d-118">CONTROL de lectura \_ (0x00020000L)</span><span class="sxs-lookup"><span data-stu-id="0925d-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="0925d-119">Necesario para leer la información del descriptor de seguridad del objeto, sin incluir la información en la SACL.</span><span class="sxs-lookup"><span data-stu-id="0925d-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="0925d-120">Para leer o escribir la SACL, debe solicitar el derecho de \_ acceso de seguridad del sistema de acceso \_ .</span><span class="sxs-lookup"><span data-stu-id="0925d-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="0925d-121">Para obtener más información, consulte [derechos de acceso de SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="0925d-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="0925d-122">SINCRONIZAr (0x00100000L)</span><span class="sxs-lookup"><span data-stu-id="0925d-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="0925d-123">No se admite para objetos de estación de ventana.</span><span class="sxs-lookup"><span data-stu-id="0925d-123">Not supported for window station objects.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="0925d-124">ESCRIBIR \_ DAC (0x00040000L)</span><span class="sxs-lookup"><span data-stu-id="0925d-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="0925d-125">Necesario para modificar la DACL en el descriptor de seguridad para el objeto.</span><span class="sxs-lookup"><span data-stu-id="0925d-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="0925d-126">Propietario de escritura \_ (0x00080000L)</span><span class="sxs-lookup"><span data-stu-id="0925d-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="0925d-127">Necesario para cambiar el propietario del descriptor de seguridad para el objeto.</span><span class="sxs-lookup"><span data-stu-id="0925d-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="0925d-128">En la tabla siguiente se enumeran los derechos de acceso específicos del objeto.</span><span class="sxs-lookup"><span data-stu-id="0925d-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="0925d-129">Derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="0925d-129">Access right</span></span>                        | <span data-ttu-id="0925d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="0925d-130">Description</span></span>                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0925d-131">WINSTA \_ todos los \_ accesos (0x37F)</span><span class="sxs-lookup"><span data-stu-id="0925d-131">WINSTA\_ALL\_ACCESS (0x37F)</span></span>         | <span data-ttu-id="0925d-132">Todos los derechos de acceso posibles para la estación de ventana.</span><span class="sxs-lookup"><span data-stu-id="0925d-132">All possible access rights for the window station.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="0925d-133">WINSTA \_ ACCESSCLIPBOARD (0x0004L)</span><span class="sxs-lookup"><span data-stu-id="0925d-133">WINSTA\_ACCESSCLIPBOARD (0x0004L)</span></span>   | <span data-ttu-id="0925d-134">Necesario para usar el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="0925d-134">Required to use the clipboard.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="0925d-135">WINSTA \_ ACCESSGLOBALATOMS (0x0020L)</span><span class="sxs-lookup"><span data-stu-id="0925d-135">WINSTA\_ACCESSGLOBALATOMS (0x0020L)</span></span> | <span data-ttu-id="0925d-136">Necesario para manipular átomos globales.</span><span class="sxs-lookup"><span data-stu-id="0925d-136">Required to manipulate global atoms.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="0925d-137">WINSTA \_ CREATEDESKTOP (0x0008L)</span><span class="sxs-lookup"><span data-stu-id="0925d-137">WINSTA\_CREATEDESKTOP (0x0008L)</span></span>     | <span data-ttu-id="0925d-138">Se requiere para crear nuevos objetos de escritorio en la estación de ventana.</span><span class="sxs-lookup"><span data-stu-id="0925d-138">Required to create new desktop objects on the window station.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="0925d-139">WINSTA \_ ENUMDESKTOPS (0x0001L)</span><span class="sxs-lookup"><span data-stu-id="0925d-139">WINSTA\_ENUMDESKTOPS (0x0001L)</span></span>      | <span data-ttu-id="0925d-140">Necesario para enumerar los objetos de escritorio existentes.</span><span class="sxs-lookup"><span data-stu-id="0925d-140">Required to enumerate existing desktop objects.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="0925d-141">\_Enumeración de WINSTA (0x0100L)</span><span class="sxs-lookup"><span data-stu-id="0925d-141">WINSTA\_ENUMERATE (0x0100L)</span></span>         | <span data-ttu-id="0925d-142">Necesario para que se Enumere la estación de ventana.</span><span class="sxs-lookup"><span data-stu-id="0925d-142">Required for the window station to be enumerated.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="0925d-143">WINSTA \_ EXITWINDOWS (0x0040L)</span><span class="sxs-lookup"><span data-stu-id="0925d-143">WINSTA\_EXITWINDOWS (0x0040L)</span></span>       | <span data-ttu-id="0925d-144">Necesario para llamar correctamente a la función [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) o [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="0925d-144">Required to successfully call the [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span> <span data-ttu-id="0925d-145">Los usuarios pueden compartir las estaciones de ventana y este tipo de acceso puede impedir que otros usuarios de una estación de ventana cierren la sesión del propietario de la estación de ventana.</span><span class="sxs-lookup"><span data-stu-id="0925d-145">Window stations can be shared by users and this access type can prevent other users of a window station from logging off the window station owner.</span></span> |
| <span data-ttu-id="0925d-146">WINSTA \_ READATTRIBUTES (0x0002L)</span><span class="sxs-lookup"><span data-stu-id="0925d-146">WINSTA\_READATTRIBUTES (0x0002L)</span></span>    | <span data-ttu-id="0925d-147">Necesario para leer los atributos de un objeto de estación de ventana.</span><span class="sxs-lookup"><span data-stu-id="0925d-147">Required to read the attributes of a window station object.</span></span> <span data-ttu-id="0925d-148">Este atributo incluye la configuración de color y otras propiedades de la estación de ventana global.</span><span class="sxs-lookup"><span data-stu-id="0925d-148">This attribute includes color settings and other global window station properties.</span></span>                                                                                                                                |
| <span data-ttu-id="0925d-149">WINSTA \_ READSCREEN (0x0200L)</span><span class="sxs-lookup"><span data-stu-id="0925d-149">WINSTA\_READSCREEN (0x0200L)</span></span>        | <span data-ttu-id="0925d-150">Necesario para tener acceso al contenido de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="0925d-150">Required to access screen contents.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="0925d-151">WINSTA \_ WRITEATTRIBUTES (0x0010L)</span><span class="sxs-lookup"><span data-stu-id="0925d-151">WINSTA\_WRITEATTRIBUTES (0x0010L)</span></span>   | <span data-ttu-id="0925d-152">Necesario para modificar los atributos de un objeto de estación de ventana.</span><span class="sxs-lookup"><span data-stu-id="0925d-152">Required to modify the attributes of a window station object.</span></span> <span data-ttu-id="0925d-153">Los atributos incluyen la configuración de color y otras propiedades de la estación de ventana global.</span><span class="sxs-lookup"><span data-stu-id="0925d-153">The attributes include color settings and other global window station properties.</span></span>                                                                                                                               |



 

<span data-ttu-id="0925d-154">A continuación se muestran los [derechos de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para el objeto de estación de ventana interactiva, que es la estación de ventana asignada a la sesión de inicio de sesión del usuario interactivo.</span><span class="sxs-lookup"><span data-stu-id="0925d-154">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the interactive window station object, which is the window station assigned to the logon session of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0925d-155">Derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="0925d-155">Access right</span></span></th>
<th><span data-ttu-id="0925d-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="0925d-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0925d-157">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="0925d-157">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="0925d-158">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="0925d-158">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="0925d-159">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="0925d-159">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="0925d-160">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="0925d-160">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="0925d-161">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="0925d-161">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="0925d-162">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="0925d-162">WINSTA_READSCREEN</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0925d-163">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="0925d-163">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="0925d-164">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="0925d-164">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="0925d-165">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="0925d-165">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="0925d-166">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="0925d-166">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="0925d-167">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="0925d-167">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0925d-168">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="0925d-168">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="0925d-169">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="0925d-169">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="0925d-170">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="0925d-170">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="0925d-171">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="0925d-171">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0925d-172">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="0925d-172">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="0925d-173">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="0925d-173">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="0925d-174">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="0925d-174">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="0925d-175">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="0925d-175">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="0925d-176">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="0925d-176">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="0925d-177">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="0925d-177">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="0925d-178">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="0925d-178">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="0925d-179">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="0925d-179">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="0925d-180">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="0925d-180">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="0925d-181">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="0925d-181">WINSTA_READSCREEN</span></span><br />
<span data-ttu-id="0925d-182">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="0925d-182">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0925d-183">A continuación se muestran los [derechos de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para un objeto de estación de ventana no interactiva.</span><span class="sxs-lookup"><span data-stu-id="0925d-183">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a noninteractive window station object.</span></span> <span data-ttu-id="0925d-184">El sistema asigna estaciones de ventana no interactivas a todas las sesiones de inicio de sesión distintas de las del usuario interactivo.</span><span class="sxs-lookup"><span data-stu-id="0925d-184">The system assigns noninteractive window stations to all logon sessions other than that of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0925d-185">Derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="0925d-185">Access right</span></span></th>
<th><span data-ttu-id="0925d-186">Descripción</span><span class="sxs-lookup"><span data-stu-id="0925d-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0925d-187">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="0925d-187">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="0925d-188">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="0925d-188">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="0925d-189">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="0925d-189">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="0925d-190">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="0925d-190">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="0925d-191">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="0925d-191">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0925d-192">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="0925d-192">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="0925d-193">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="0925d-193">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="0925d-194">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="0925d-194">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="0925d-195">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="0925d-195">WINSTA_CREATEDESKTOP</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0925d-196">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="0925d-196">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="0925d-197">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="0925d-197">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="0925d-198">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="0925d-198">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="0925d-199">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="0925d-199">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0925d-200">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="0925d-200">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="0925d-201">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="0925d-201">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="0925d-202">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="0925d-202">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="0925d-203">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="0925d-203">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="0925d-204">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="0925d-204">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="0925d-205">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="0925d-205">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="0925d-206">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="0925d-206">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="0925d-207">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="0925d-207">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="0925d-208">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="0925d-208">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0925d-209">Puede solicitar el derecho de \_ acceso de seguridad del sistema de acceso \_ a un objeto de estación de ventana si desea leer o escribir la SACL del objeto.</span><span class="sxs-lookup"><span data-stu-id="0925d-209">You can request the ACCESS\_SYSTEM\_SECURITY access right to a window station object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="0925d-210">Para obtener más información, consulte derechos [de acceso de las listas de control de acceso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) y [SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="0925d-210">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 