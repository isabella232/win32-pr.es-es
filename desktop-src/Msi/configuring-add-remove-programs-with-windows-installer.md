---
description: Puede proporcionar toda la información necesaria para configurar agregar o quitar programas en el panel de control estableciendo los valores de determinadas propiedades del instalador en el paquete de Windows Installer de la aplicación.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Configuración de agregar o quitar programas con Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6850163e18af94aa9cceaf6c4bb2e8059dcf2121
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/30/2021
ms.locfileid: "105994507"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a><span data-ttu-id="4fe69-103">Configuración de agregar o quitar programas con Windows Installer</span><span class="sxs-lookup"><span data-stu-id="4fe69-103">Configuring Add/Remove Programs with Windows Installer</span></span>

<span data-ttu-id="4fe69-104">Puede proporcionar toda la información necesaria para configurar agregar o quitar programas en el panel de control estableciendo los valores de determinadas propiedades del instalador en el paquete de Windows Installer de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fe69-104">You can supply all of the information needed to configure Add/Remove Programs in Control Panel by setting the values of certain installer properties in your application's Windows Installer package.</span></span> <span data-ttu-id="4fe69-105">Al establecer estas propiedades, se escriben automáticamente los valores correspondientes en el registro.</span><span class="sxs-lookup"><span data-stu-id="4fe69-105">Setting these properties automatically writes the corresponding values into the registry.</span></span> <span data-ttu-id="4fe69-106">Si el instalador detecta que el producto está marcado para su eliminación completa, las operaciones se agregan automáticamente al script para quitar la carpeta agregar o quitar programas en la información del panel de control del producto.</span><span class="sxs-lookup"><span data-stu-id="4fe69-106">If the installer detects that the product is marked for complete removal, operations are automatically added to the script to remove the Add/Remove Programs folder in Control Panel information for the product.</span></span>

<span data-ttu-id="4fe69-107">Si una aplicación no está registrada, no aparece en Agregar o quitar programas en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="4fe69-107">If an application is not registered, it is not listed in Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="4fe69-108">Para obtener más información, vea [Agregar y quitar una aplicación y no dejar ningún seguimiento en el registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="4fe69-108">For more information, see [Adding and Removing an Application and Leaving No Trace in the Registry](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).</span></span>

<span data-ttu-id="4fe69-109">Las aplicaciones que se han instalado en el contexto de [instalación](installation-context.md) por usuario se muestran en Agregar o quitar programas del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="4fe69-109">Applications that have been installed in the per-user [installation context](installation-context.md) are displayed in the Add/Remove Programs of the current user.</span></span> <span data-ttu-id="4fe69-110">Las aplicaciones que se han instalado en el contexto de instalación por equipo se muestran en Agregar o quitar programas de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="4fe69-110">Applications that have been installed in the per-machine installation context are displayed in the Add/Remove Programs of all users.</span></span> <span data-ttu-id="4fe69-111">Las aplicaciones que no se han instalado por equipo y que solo se han instalado como aplicaciones por usuario para los usuarios que no son el usuario actual, no aparecen en Agregar o quitar programas del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="4fe69-111">Applications that have not been installed per-machine, and have only been installed as per-user applications for users other than the current user, do not appear in the Add/Remove Programs of the current user.</span></span>

<span data-ttu-id="4fe69-112">Tenga en cuenta que los paquetes de instalación que usan la propiedad [**LIMITUI**](limitui.md) también deben contener [**ARPNOMODIFY**](arpnomodify.md).</span><span class="sxs-lookup"><span data-stu-id="4fe69-112">Note that installation packages that use the [**LIMITUI**](limitui.md) property must also contain the [**ARPNOMODIFY**](arpnomodify.md).</span></span> <span data-ttu-id="4fe69-113">Esto es necesario para que un usuario obtenga el comportamiento correcto en Agregar o quitar programas en la utilidad del panel de control al intentar configurar un producto.</span><span class="sxs-lookup"><span data-stu-id="4fe69-113">This is required for a user to obtain the correct behavior from Add/Remove Programs in Control Panel utility when attempting to configure a product.</span></span>

<span data-ttu-id="4fe69-114">El instalador usa las siguientes [propiedades públicas](public-properties.md) para administrar agregar o quitar programas en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="4fe69-114">The installer uses the following [public properties](public-properties.md) to manage Add/Remove Programs in Control Panel.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4fe69-115">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="4fe69-115">Property name</span></span></th>
<th><span data-ttu-id="4fe69-116">Breve descripción de la propiedad</span><span class="sxs-lookup"><span data-stu-id="4fe69-116">Brief description of property</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4fe69-117"><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-117"><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-118">Dirección URL del canal de actualización para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fe69-118">URL of the update channel for the application.</span></span> <span data-ttu-id="4fe69-119">Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</span><span class="sxs-lookup"><span data-stu-id="4fe69-119">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fe69-120"><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-120"><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-121">Proporciona comentarios para agregar o quitar programas en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="4fe69-121">Provides Comments for the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="4fe69-122">Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</span><span class="sxs-lookup"><span data-stu-id="4fe69-122">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fe69-123"><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-123"><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-124">Proporciona el contacto para agregar o quitar programas en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="4fe69-124">Provides the Contact for Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="4fe69-125">Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</span><span class="sxs-lookup"><span data-stu-id="4fe69-125">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fe69-126"><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-126"><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-127">Ruta de acceso completa a la carpeta principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fe69-127">Fully qualified path to the application's primary folder.</span></span> <span data-ttu-id="4fe69-128">Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</span><span class="sxs-lookup"><span data-stu-id="4fe69-128">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fe69-129"><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-129"><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-130">Dirección de Internet, o dirección URL, para obtener soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="4fe69-130">Internet address, or URL, for technical support.</span></span> <span data-ttu-id="4fe69-131">Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</span><span class="sxs-lookup"><span data-stu-id="4fe69-131">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fe69-132"><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-132"><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-133">Números de teléfono de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="4fe69-133">Technical support phone numbers.</span></span> <span data-ttu-id="4fe69-134">Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</span><span class="sxs-lookup"><span data-stu-id="4fe69-134">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fe69-135"><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-135"><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-136">Impide que se muestre un botón cambiar para el producto en Agregar o quitar programas en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="4fe69-136">Prevents display of a Change button for the product in Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="4fe69-137">
<b>Nota:</b> Esto solo afecta a la presentación en el ARP.</span><span class="sxs-lookup"><span data-stu-id="4fe69-137">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="4fe69-138">El Windows Installer todavía es capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.</span><span class="sxs-lookup"><span data-stu-id="4fe69-138">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fe69-139"><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-139"><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-140">Impide que se muestre un botón Quitar del producto en Agregar o quitar programas en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="4fe69-140">Prevents display of a Remove button for the product in the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="4fe69-141">El producto aún se puede quitar si se selecciona el botón cambiar si el paquete de instalación se ha creado con una interfaz de usuario que proporciona la eliminación del producto como opción.</span><span class="sxs-lookup"><span data-stu-id="4fe69-141">The product can still be removed by selecting the Change button if the installation package has been authored with a user interface that provides product removal as an option.</span></span>
<blockquote><span data-ttu-id="4fe69-142">
<b>Nota:</b> Esto solo afecta a la presentación en el ARP.</span><span class="sxs-lookup"><span data-stu-id="4fe69-142">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="4fe69-143">El Windows Installer todavía es capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.</span><span class="sxs-lookup"><span data-stu-id="4fe69-143">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fe69-144"><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-144"><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-145">Deshabilita el botón reparar en Agregar o quitar programas en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="4fe69-145">Disables the Repair button in the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="4fe69-146">
<b>Nota:</b> Esto solo afecta a la presentación en el ARP.</span><span class="sxs-lookup"><span data-stu-id="4fe69-146">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="4fe69-147">El Windows Installer todavía es capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.</span><span class="sxs-lookup"><span data-stu-id="4fe69-147">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fe69-148"><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-148"><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-149">Identifica el icono que se muestra en Agregar o quitar programas.</span><span class="sxs-lookup"><span data-stu-id="4fe69-149">Identifies the icon displayed in Add/Remove Programs.</span></span> <span data-ttu-id="4fe69-150">Si no se define esta propiedad, agregar o quitar programas especifica el icono de presentación.</span><span class="sxs-lookup"><span data-stu-id="4fe69-150">If this property is not defined, Add/Remove Programs specifies the display icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fe69-151"><a href="arpreadme.md"><strong>ARPREADME</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-151"><a href="arpreadme.md"><strong>ARPREADME</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-152">Proporciona el archivo Léame para agregar o quitar programas en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="4fe69-152">Provides the ReadMe for Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="4fe69-153">Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</span><span class="sxs-lookup"><span data-stu-id="4fe69-153">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fe69-154"><a href="arpsize.md"><strong>ARPSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-154"><a href="arpsize.md"><strong>ARPSIZE</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-155">Tamaño estimado de la aplicación en KB.</span><span class="sxs-lookup"><span data-stu-id="4fe69-155">Estimated size of the application in KB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fe69-156"><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-156"><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-157">Impide que la aplicación se muestre en la lista programas de agregar o quitar programas en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="4fe69-157">Prevents display of the application in the Programs List of the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="4fe69-158">
<b>Nota:</b> Esto solo afecta a la presentación en el ARP.</span><span class="sxs-lookup"><span data-stu-id="4fe69-158">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="4fe69-159">El Windows Installer todavía es capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.</span><span class="sxs-lookup"><span data-stu-id="4fe69-159">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fe69-160"><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-160"><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-161">Dirección URL de la Página principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fe69-161">URL for application's home page.</span></span> <span data-ttu-id="4fe69-162">Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</span><span class="sxs-lookup"><span data-stu-id="4fe69-162">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fe69-163"><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="4fe69-163"><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></span></span></td>
<td><span data-ttu-id="4fe69-164">Dirección URL para la información de actualización de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fe69-164">URL for application update information.</span></span> <span data-ttu-id="4fe69-165">Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</span><span class="sxs-lookup"><span data-stu-id="4fe69-165">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
</tbody>
</table>

> [!Note]  
> <span data-ttu-id="4fe69-166">Para obtener información sobre la herramienta establecer programa y valores predeterminados, consulte la sección [trabajar con configurar acceso y programas predeterminados del equipo](/previous-versions//bb776877(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4fe69-166">For information regarding the Set Program and Defaults tool, refer to the section [Working with Set Program Access and Computer Defaults](/previous-versions//bb776877(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fe69-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4fe69-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fe69-168">Desinstalar la clave del registro</span><span class="sxs-lookup"><span data-stu-id="4fe69-168">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
</dt> </dl>
