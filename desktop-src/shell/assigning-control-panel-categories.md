---
description: A partir de Windows XP, el panel de control admite la categorización de elementos del panel de control. Los elementos se registran para aparecer en una o varias categorías. No se pueden crear nuevas categorías.
title: Asignar categorías del panel de control
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bade62cda23c2d2f66ffdfd70f3f555a243f3efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984363"
---
# <a name="assigning-control-panel-categories"></a><span data-ttu-id="c988b-105">Asignar categorías del panel de control</span><span class="sxs-lookup"><span data-stu-id="c988b-105">Assigning Control Panel Categories</span></span>

<span data-ttu-id="c988b-106">A partir de Windows XP, el panel de control admite la categorización de elementos del panel de control.</span><span class="sxs-lookup"><span data-stu-id="c988b-106">As of Windows XP, Control Panel supports categorization of Control Panel items.</span></span> <span data-ttu-id="c988b-107">Los elementos se registran para aparecer en una o varias categorías.</span><span class="sxs-lookup"><span data-stu-id="c988b-107">Items are registered to appear in one or more category.</span></span> <span data-ttu-id="c988b-108">No se pueden crear nuevas categorías.</span><span class="sxs-lookup"><span data-stu-id="c988b-108">New categories cannot be created.</span></span>

<span data-ttu-id="c988b-109">Para registrar un elemento del panel de control en una o varias categorías, agregue valores como se explica en la sección registro de elementos del panel de [control ejecutable](registering-control-panel-items.md) o registro de elementos del panel de control de [dll](registering-control-panel-items.md) de registro de [elementos del panel](registering-control-panel-items.md)de control, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="c988b-109">To register a Control Panel item in one or more categories, add values as explained in the [Executable Control Panel Item Registration](registering-control-panel-items.md) or [DLL Control Panel Item Registration](registering-control-panel-items.md) section of [Registering Control Panel Items](registering-control-panel-items.md), as appropriate.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c988b-110">Id. de categoría</span><span class="sxs-lookup"><span data-stu-id="c988b-110">Category ID</span></span></th>
<th><span data-ttu-id="c988b-111">Nombre de categoría (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="c988b-111">Category Name (Windows 7)</span></span></th>
<th><span data-ttu-id="c988b-112">Nombre de categoría (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="c988b-112">Category Name (Windows Vista)</span></span></th>
<th><span data-ttu-id="c988b-113">Nombre de categoría (Windows XP)</span><span class="sxs-lookup"><span data-stu-id="c988b-113">Category Name (Windows XP)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c988b-114">0</span><span class="sxs-lookup"><span data-stu-id="c988b-114">0</span></span></td>
<td><span data-ttu-id="c988b-115">&quot;Todos los elementos del panel de control&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-115">&quot;All Control Panel Items&quot;</span></span></td>
<td><span data-ttu-id="c988b-116">&quot;Opciones adicionales&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-116">&quot;Additional Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c988b-117">En esta categoría aparece cualquier elemento del panel de control que no especifique un ID. de categoría.</span><span class="sxs-lookup"><span data-stu-id="c988b-117">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="c988b-118">&quot;Otras opciones del panel de control&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-118">&quot;Other Control Panel Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c988b-119">En esta categoría aparece cualquier elemento del panel de control que no especifique un ID. de categoría.</span><span class="sxs-lookup"><span data-stu-id="c988b-119">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c988b-120">1</span><span class="sxs-lookup"><span data-stu-id="c988b-120">1</span></span></td>
<td><span data-ttu-id="c988b-121">&quot;Apariencia y personalización&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-121">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="c988b-122">&quot;Apariencia y personalización&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-122">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="c988b-123">&quot;Apariencia y temas&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-123">&quot;Appearance and Themes&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c988b-124">2</span><span class="sxs-lookup"><span data-stu-id="c988b-124">2</span></span></td>
<td><span data-ttu-id="c988b-125">&quot;Hardware y sonido&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-125">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="c988b-126">&quot;Hardware y sonido&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-126">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="c988b-127">&quot;Impresoras y otro hardware&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-127">&quot;Printers and Other Hardware&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c988b-128">3</span><span class="sxs-lookup"><span data-stu-id="c988b-128">3</span></span></td>
<td><span data-ttu-id="c988b-129">&quot;Red e Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-129">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="c988b-130">&quot;Red e Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-130">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="c988b-131">&quot;Conexiones de red e Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-131">&quot;Network and Internet Connections&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c988b-132">4</span><span class="sxs-lookup"><span data-stu-id="c988b-132">4</span></span></td>
<td><span data-ttu-id="c988b-133">Ya no se usa.</span><span class="sxs-lookup"><span data-stu-id="c988b-133">No longer used.</span></span> <span data-ttu-id="c988b-134">Los elementos que se agregan solo a la categoría 4 aparecen en categoría 2 (hardware y sonido).</span><span class="sxs-lookup"><span data-stu-id="c988b-134">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="c988b-135">Ya no se usa.</span><span class="sxs-lookup"><span data-stu-id="c988b-135">No longer used.</span></span> <span data-ttu-id="c988b-136">Los elementos que se agregan solo a la categoría 4 aparecen en categoría 2 (hardware y sonido).</span><span class="sxs-lookup"><span data-stu-id="c988b-136">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="c988b-137">&quot;Dispositivos de sonido, voz y audio&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-137">&quot;Sounds, Speech, and Audio Devices&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c988b-138">5</span><span class="sxs-lookup"><span data-stu-id="c988b-138">5</span></span></td>
<td><span data-ttu-id="c988b-139">&quot;Sistema y seguridad&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-139">&quot;System and Security&quot;</span></span></td>
<td><span data-ttu-id="c988b-140">&quot;Sistema y mantenimiento&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-140">&quot;System and Maintenance&quot;</span></span></td>
<td><span data-ttu-id="c988b-141">&quot;Rendimiento y mantenimiento&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-141">&quot;Performance and Maintenance&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c988b-142">6</span><span class="sxs-lookup"><span data-stu-id="c988b-142">6</span></span></td>
<td><span data-ttu-id="c988b-143">&quot;Reloj, idioma y región&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-143">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="c988b-144">&quot;Reloj, idioma y región&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-144">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="c988b-145">&quot;Opciones de fecha, hora, idioma y configuración regional&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-145">&quot;Date, Time, Language, and Regional Options&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c988b-146">7</span><span class="sxs-lookup"><span data-stu-id="c988b-146">7</span></span></td>
<td><span data-ttu-id="c988b-147">&quot;Facilidad de acceso&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-147">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="c988b-148">&quot;Facilidad de acceso&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-148">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="c988b-149">&quot;Opciones de accesibilidad&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-149">&quot;Accessibility Options&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c988b-150">8</span><span class="sxs-lookup"><span data-stu-id="c988b-150">8</span></span></td>
<td><span data-ttu-id="c988b-151">&quot;Programs&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-151">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="c988b-152">&quot;Programs&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-152">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="c988b-153">&quot;Agregar o quitar programas&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-153">&quot;Add or Remove Programs&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c988b-154">9</span><span class="sxs-lookup"><span data-stu-id="c988b-154">9</span></span></td>
<td><span data-ttu-id="c988b-155">&quot;Cuentas de usuario&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-155">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c988b-156">Cuando no está conectado a un dominio, esto se denomina &quot; cuentas de usuario y seguridad de la familia &quot; .</span><span class="sxs-lookup"><span data-stu-id="c988b-156">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="c988b-157">&quot;Cuentas de usuario&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-157">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c988b-158">Cuando no está conectado a un dominio, esto se denomina &quot; cuentas de usuario y seguridad de la familia &quot; .</span><span class="sxs-lookup"><span data-stu-id="c988b-158">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="c988b-159">&quot;Cuentas de usuario&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-159">&quot;User Accounts&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c988b-160">10</span><span class="sxs-lookup"><span data-stu-id="c988b-160">10</span></span></td>
<td><span data-ttu-id="c988b-161">Ya no se usa.</span><span class="sxs-lookup"><span data-stu-id="c988b-161">No longer used.</span></span> <span data-ttu-id="c988b-162">Los elementos registrados en esta categoría aparecen en categoría 5 (sistema y seguridad).</span><span class="sxs-lookup"><span data-stu-id="c988b-162">Items registered in this category appear in category 5 (System and Security).</span></span></td>
<td><span data-ttu-id="c988b-163">&quot;Seguridad&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-163">&quot;Security&quot;</span></span></td>
<td><span data-ttu-id="c988b-164">&quot;Centro de seguridad&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-164">&quot;Security Center&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c988b-165">Solo disponible en Windows XP Service Pack 2 (SP2) o posterior.</span><span class="sxs-lookup"><span data-stu-id="c988b-165">Available only in Windows XP Service Pack 2 (SP2) or later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c988b-166">11</span><span class="sxs-lookup"><span data-stu-id="c988b-166">11</span></span></td>
<td><span data-ttu-id="c988b-167">Ya no se usa.</span><span class="sxs-lookup"><span data-stu-id="c988b-167">No longer used.</span></span> <span data-ttu-id="c988b-168">Los elementos registrados en esta categoría aparecen en la categoría 0 (todos los elementos del panel de control).</span><span class="sxs-lookup"><span data-stu-id="c988b-168">Items registered in this category appear in category 0 (All Control Panel Items).</span></span></td>
<td><span data-ttu-id="c988b-169">&quot;PC móvil&quot;</span><span class="sxs-lookup"><span data-stu-id="c988b-169">&quot;Mobile PC&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c988b-170">Esta categoría solo está visible en PC móviles.</span><span class="sxs-lookup"><span data-stu-id="c988b-170">This category is only visible on mobile PCs.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="c988b-171">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c988b-171">Not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c988b-172">En Windows XP, las categorías **Agregar o quitar programas** y **cuentas de usuario** funcionan de forma ligeramente diferente a otras categorías del panel de control.</span><span class="sxs-lookup"><span data-stu-id="c988b-172">In Windows XP, the categories **Add or Remove Programs** and **User Accounts** work somewhat differently from other categories in Control Panel.</span></span> <span data-ttu-id="c988b-173">Cuando se agregan uno o varios elementos a una de estas dos categorías, el vínculo asociado del panel de control abre una página de categorías.</span><span class="sxs-lookup"><span data-stu-id="c988b-173">When one or more items are added to one of these two categories, the associated link in Control Panel opens a category page.</span></span> <span data-ttu-id="c988b-174">Los elementos registrados aparecen en la parte inferior de la página bajo el encabezado "o seleccionar un icono del panel de control".</span><span class="sxs-lookup"><span data-stu-id="c988b-174">The registered items appear in the lower portion of the page under the heading "or Pick a Control Panel icon".</span></span> <span data-ttu-id="c988b-175">Cuando no se registra ningún elemento para una de estas categorías, el vínculo asociado del panel de control invoca directamente el elemento estándar de Windows para esa categoría.</span><span class="sxs-lookup"><span data-stu-id="c988b-175">When no items are registered for one of these categories, the associated link in Control Panel directly invokes the standard Windows item for that category.</span></span> <span data-ttu-id="c988b-176">En Windows Vista y versiones posteriores, la categoría **programas** y la categoría **cuentas de usuario** no tienen esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c988b-176">In Windows Vista and later, the **Programs** category and the **User Accounts** category do not have this property.</span></span>

<span data-ttu-id="c988b-177">La categoría **Security Center** , disponible únicamente en Windows XP SP2, también es algo no estándar.</span><span class="sxs-lookup"><span data-stu-id="c988b-177">The **Security Center** category, available only in Windows XP SP2, is also somewhat non-standard.</span></span> <span data-ttu-id="c988b-178">Al hacer clic en esta categoría, se abre la página **Security Center** en una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="c988b-178">Clicking this category opens the **Security Center** page in a new window.</span></span> <span data-ttu-id="c988b-179">Los elementos registrados para **Security Center** aparecen en la parte inferior de la página en el encabezado **administrar la configuración de seguridad de:**.</span><span class="sxs-lookup"><span data-stu-id="c988b-179">Items registered for **Security Center** appear in the lower portion of that page under the heading **Manage security settings for:**.</span></span> <span data-ttu-id="c988b-180">Al hacer clic en un icono, se abre el elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="c988b-180">Clicking an icon opens the Control Panel item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c988b-181">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c988b-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c988b-182">Elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="c988b-182">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="c988b-183">Directrices de la experiencia de usuario</span><span class="sxs-lookup"><span data-stu-id="c988b-183">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="c988b-184">Registrar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="c988b-184">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="c988b-185">Usar CPLApplet</span><span class="sxs-lookup"><span data-stu-id="c988b-185">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="c988b-186">Procesamiento de mensajes del panel de control</span><span class="sxs-lookup"><span data-stu-id="c988b-186">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="c988b-187">Ejecutar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="c988b-187">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="c988b-188">Extender elementos del panel de control del sistema</span><span class="sxs-lookup"><span data-stu-id="c988b-188">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="c988b-189">Crear vínculos de tarea que se pueden buscar para un elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="c988b-189">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="c988b-190">Acceder al panel de control en modo seguro en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c988b-190">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




