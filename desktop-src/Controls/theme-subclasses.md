---
title: Usar subclases de tema
description: Se pueden crear subclases para las clases de tema que representan controles como ComboBox, Edit, ExplorerBar, Rebar, Tab y Toolbar con el fin de proporcionar variaciones de tema para ese control concreto.
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c5448bb5fea90193beed854e833cd34e7691b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775583"
---
# <a name="using-theme-subclasses"></a><span data-ttu-id="10cf8-103">Usar subclases de tema</span><span class="sxs-lookup"><span data-stu-id="10cf8-103">Using Theme Subclasses</span></span>

<span data-ttu-id="10cf8-104">Se pueden crear subclases para las clases de tema que representan controles como ComboBox, Edit, ExplorerBar, Rebar, Tab y Toolbar con el fin de proporcionar variaciones de tema para ese control concreto.</span><span class="sxs-lookup"><span data-stu-id="10cf8-104">Theme classes that represent controls such as ComboBox, Edit, ExplorerBar, Rebar, Tab, and Toolbar can be subclassed in order to provide theme variations for that particular control.</span></span> <span data-ttu-id="10cf8-105">Por ejemplo, la clase **Button** se subclase como `Start::Button` para proporcionar control sobre el tema que se aplica al botón **iniciar** .</span><span class="sxs-lookup"><span data-stu-id="10cf8-105">For example, the **Button** class is subclassed as `Start::Button` in order to provide control over the theme applied to the **Start** button.</span></span>

> [!Note]  
> <span data-ttu-id="10cf8-106">Tenga cuidado al crear subclases como las que se describen en este tema.</span><span class="sxs-lookup"><span data-stu-id="10cf8-106">Use caution when you create subclasses like those that are discussed in this topic.</span></span> <span data-ttu-id="10cf8-107">Dado que las subclases podrían modificarse o no estar disponibles en versiones posteriores de Windows, no se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="10cf8-107">Because subclasses might be altered or unavailable in subsequent versions of Windows, you are discouraged from using them.</span></span>

 

## <a name="two-ways-to-use-a-theme-subclass"></a><span data-ttu-id="10cf8-108">Dos maneras de utilizar una subclase Theme</span><span class="sxs-lookup"><span data-stu-id="10cf8-108">Two Ways to Use a Theme Subclass</span></span>

<span data-ttu-id="10cf8-109">Una aplicación puede utilizar un tema de subclases de una de estas dos maneras:</span><span class="sxs-lookup"><span data-stu-id="10cf8-109">An application can use a subclassed theme in one of these two ways:</span></span>

-   <span data-ttu-id="10cf8-110">Puede usar la función [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) con una cadena del formulario `subclass::class` en el parámetro *pszClassList* .</span><span class="sxs-lookup"><span data-stu-id="10cf8-110">It can use the [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) function with a string of the form `subclass::class` in the *pszClassList* parameter.</span></span>
-   <span data-ttu-id="10cf8-111">Puede llamar a [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) con el nombre de subclase de tema en el parámetro *pszSubAppName* .</span><span class="sxs-lookup"><span data-stu-id="10cf8-111">It can call [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) with the theme subclass name in the *pszSubAppName* parameter.</span></span>

## <a name="using-theme-messages-that-set-visual-style"></a><span data-ttu-id="10cf8-112">Usar mensajes de tema que establecen el estilo visual</span><span class="sxs-lookup"><span data-stu-id="10cf8-112">Using Theme Messages That Set Visual Style</span></span>

<span data-ttu-id="10cf8-113">Algunos controles, como rebar y Toolbar, proporcionan mensajes específicos que puede enviar para indicar al control que use una subclase de tema.</span><span class="sxs-lookup"><span data-stu-id="10cf8-113">Certain controls, such as Rebar and Toolbar, provide specific messages that you can send to instruct the control to use a theme subclass.</span></span> <span data-ttu-id="10cf8-114">Para esos controles, proporcione un puntero a un búfer que contenga el nombre de subclase del tema en el parámetro *lParam* del mensaje.</span><span class="sxs-lookup"><span data-stu-id="10cf8-114">For those controls, provide a pointer to a buffer that contains the theme subclass name in the *lParam* parameter of the message.</span></span> <span data-ttu-id="10cf8-115">Use el mensaje [**\_ SETWINDOWTHEME de CCM**](ccm-setwindowtheme.md) genérico o use una variante específica, como la que se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="10cf8-115">Use the generic [**CCM\_SETWINDOWTHEME**](ccm-setwindowtheme.md) message, or use a specific variant like those shown in the following table.</span></span>



| <span data-ttu-id="10cf8-116">Control</span><span class="sxs-lookup"><span data-stu-id="10cf8-116">Control</span></span>    | <span data-ttu-id="10cf8-117">Message</span><span class="sxs-lookup"><span data-stu-id="10cf8-117">Message</span></span>                                             |
|------------|-----------------------------------------------------|
| <span data-ttu-id="10cf8-118">Información sobre herramientas</span><span class="sxs-lookup"><span data-stu-id="10cf8-118">Tooltip</span></span>    | [<span data-ttu-id="10cf8-119">**TTM \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="10cf8-119">**TTM\_SETWINDOWTHEME**</span></span>](ttm-setwindowtheme.md)   |
| <span data-ttu-id="10cf8-120">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="10cf8-120">Toolbar</span></span>    | [<span data-ttu-id="10cf8-121">**TB \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="10cf8-121">**TB\_SETWINDOWTHEME**</span></span>](tb-setwindowtheme.md)     |
| <span data-ttu-id="10cf8-122">Rebar</span><span class="sxs-lookup"><span data-stu-id="10cf8-122">Rebar</span></span>      | [<span data-ttu-id="10cf8-123">**\_SETWINDOWTHEME RB**</span><span class="sxs-lookup"><span data-stu-id="10cf8-123">**RB\_SETWINDOWTHEME**</span></span>](rb-setwindowtheme.md)     |
| <span data-ttu-id="10cf8-124">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="10cf8-124">ComboBoxEx</span></span> | [<span data-ttu-id="10cf8-125">**CBEM \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="10cf8-125">**CBEM\_SETWINDOWTHEME**</span></span>](cbem-setwindowtheme.md) |



 

<span data-ttu-id="10cf8-126">En la tabla siguiente se enumeran algunas de las subclases que define Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="10cf8-126">The following table lists some of the subclasses that Windows Vista defines.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10cf8-127">Clase</span><span class="sxs-lookup"><span data-stu-id="10cf8-127">Class</span></span></th>
<th><span data-ttu-id="10cf8-128">Subclases </span><span class="sxs-lookup"><span data-stu-id="10cf8-128">Subclasses</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10cf8-129">ComboBox</span><span class="sxs-lookup"><span data-stu-id="10cf8-129">ComboBox</span></span></td>
<td><ul>
<li><span data-ttu-id="10cf8-130">Dirección</span><span class="sxs-lookup"><span data-stu-id="10cf8-130">Address</span></span></li>
<li><span data-ttu-id="10cf8-131">AddressComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-131">AddressComposited</span></span></li>
<li><span data-ttu-id="10cf8-132">InactiveAddress</span><span class="sxs-lookup"><span data-stu-id="10cf8-132">InactiveAddress</span></span></li>
<li><span data-ttu-id="10cf8-133">InactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-133">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="10cf8-134">MaxAddress</span><span class="sxs-lookup"><span data-stu-id="10cf8-134">MaxAddress</span></span></li>
<li><span data-ttu-id="10cf8-135">MaxAddressComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-135">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="10cf8-136">MaxInactiveAddress</span><span class="sxs-lookup"><span data-stu-id="10cf8-136">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="10cf8-137">MaxInactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-137">MaxInactiveAddressComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10cf8-138">Editar</span><span class="sxs-lookup"><span data-stu-id="10cf8-138">Edit</span></span></td>
<td><ul>
<li><span data-ttu-id="10cf8-139">Dirección</span><span class="sxs-lookup"><span data-stu-id="10cf8-139">Address</span></span></li>
<li><span data-ttu-id="10cf8-140">AddressComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-140">AddressComposited</span></span></li>
<li><span data-ttu-id="10cf8-141">InactiveAddress</span><span class="sxs-lookup"><span data-stu-id="10cf8-141">InactiveAddress</span></span></li>
<li><span data-ttu-id="10cf8-142">InactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-142">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="10cf8-143">InactiveSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="10cf8-143">InactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="10cf8-144">InactiveSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-144">InactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="10cf8-145">MaxAddress</span><span class="sxs-lookup"><span data-stu-id="10cf8-145">MaxAddress</span></span></li>
<li><span data-ttu-id="10cf8-146">MaxAddressComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-146">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="10cf8-147">MaxInactiveAddress</span><span class="sxs-lookup"><span data-stu-id="10cf8-147">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="10cf8-148">MaxInactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-148">MaxInactiveAddressComposited</span></span></li>
<li><span data-ttu-id="10cf8-149">MaxInactiveSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="10cf8-149">MaxInactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="10cf8-150">MaxInactiveSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-150">MaxInactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="10cf8-151">MaxSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="10cf8-151">MaxSearchBoxEdit</span></span></li>
<li><span data-ttu-id="10cf8-152">MaxSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-152">MaxSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="10cf8-153">SearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="10cf8-153">SearchBoxEdit</span></span></li>
<li><span data-ttu-id="10cf8-154">SearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-154">SearchBoxEditComposited</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10cf8-155">Rebar</span><span class="sxs-lookup"><span data-stu-id="10cf8-155">Rebar</span></span></td>
<td><ul>
<li><span data-ttu-id="10cf8-156">BrowserTabBar</span><span class="sxs-lookup"><span data-stu-id="10cf8-156">BrowserTabBar</span></span></li>
<li><span data-ttu-id="10cf8-157">InactiveNavbar</span><span class="sxs-lookup"><span data-stu-id="10cf8-157">InactiveNavbar</span></span></li>
<li><span data-ttu-id="10cf8-158">InactiveNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-158">InactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="10cf8-159">MaxInactiveNavbar</span><span class="sxs-lookup"><span data-stu-id="10cf8-159">MaxInactiveNavbar</span></span></li>
<li><span data-ttu-id="10cf8-160">MaxInactiveNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-160">MaxInactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="10cf8-161">MaxNavbar</span><span class="sxs-lookup"><span data-stu-id="10cf8-161">MaxNavbar</span></span></li>
<li><span data-ttu-id="10cf8-162">MaxNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-162">MaxNavbarComposited</span></span></li>
<li><span data-ttu-id="10cf8-163">Barra de navegación</span><span class="sxs-lookup"><span data-stu-id="10cf8-163">Navbar</span></span></li>
<li><span data-ttu-id="10cf8-164">NavbarComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-164">NavbarComposited</span></span></li>
<li><span data-ttu-id="10cf8-165">NavbarNonTopmost</span><span class="sxs-lookup"><span data-stu-id="10cf8-165">NavbarNonTopmost</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10cf8-166">Pestaña</span><span class="sxs-lookup"><span data-stu-id="10cf8-166">Tab</span></span></td>
<td><ul>
<li><span data-ttu-id="10cf8-167">BrowserTab</span><span class="sxs-lookup"><span data-stu-id="10cf8-167">BrowserTab</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10cf8-168">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="10cf8-168">Toolbar</span></span></td>
<td><ul>
<li><span data-ttu-id="10cf8-169">Go</span><span class="sxs-lookup"><span data-stu-id="10cf8-169">Go</span></span></li>
<li><span data-ttu-id="10cf8-170">GoComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-170">GoComposited</span></span></li>
<li><span data-ttu-id="10cf8-171">InactiveGo</span><span class="sxs-lookup"><span data-stu-id="10cf8-171">InactiveGo</span></span></li>
<li><span data-ttu-id="10cf8-172">InactiveGoComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-172">InactiveGoComposited</span></span></li>
<li><span data-ttu-id="10cf8-173">MaxGo</span><span class="sxs-lookup"><span data-stu-id="10cf8-173">MaxGo</span></span></li>
<li><span data-ttu-id="10cf8-174">MaxGoComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-174">MaxGoComposited</span></span></li>
<li><span data-ttu-id="10cf8-175">MaxInactiveGo</span><span class="sxs-lookup"><span data-stu-id="10cf8-175">MaxInactiveGo</span></span></li>
<li><span data-ttu-id="10cf8-176">MaxInactiveGoComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-176">MaxInactiveGoComposited</span></span></li>
<li><span data-ttu-id="10cf8-177">SearchButton</span><span class="sxs-lookup"><span data-stu-id="10cf8-177">SearchButton</span></span></li>
<li><span data-ttu-id="10cf8-178">SearchButtonComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-178">SearchButtonComposited</span></span></li>
<li><span data-ttu-id="10cf8-179">Viajes</span><span class="sxs-lookup"><span data-stu-id="10cf8-179">Travel</span></span></li>
<li><span data-ttu-id="10cf8-180">TravelComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-180">TravelComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="internet-explorer-subclasses"></a><span data-ttu-id="10cf8-181">Subclases de Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="10cf8-181">Internet Explorer Subclasses</span></span>

<span data-ttu-id="10cf8-182">En Windows Vista, las subclases de ciertas clases internas en Windows Internet Explorer y el explorador de Windows están disponibles aunque no sean las propias clases.</span><span class="sxs-lookup"><span data-stu-id="10cf8-182">In Windows Vista, the subclasses of certain classes internal to Windows Internet Explorer and Windows Explorer are available even though the classes themselves are not.</span></span> <span data-ttu-id="10cf8-183">En la tabla siguiente se enumeran las subclases disponibles.</span><span class="sxs-lookup"><span data-stu-id="10cf8-183">The following table lists the available subclasses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10cf8-184">AddressBand</span><span class="sxs-lookup"><span data-stu-id="10cf8-184">AddressBand</span></span></td>
<td><ul>
<li><span data-ttu-id="10cf8-185">AB</span><span class="sxs-lookup"><span data-stu-id="10cf8-185">AB</span></span></li>
<li><span data-ttu-id="10cf8-186">ABGreen</span><span class="sxs-lookup"><span data-stu-id="10cf8-186">ABGreen</span></span></li>
<li><span data-ttu-id="10cf8-187">ABGreenComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-187">ABGreenComposited</span></span></li>
<li><span data-ttu-id="10cf8-188">ABRed</span><span class="sxs-lookup"><span data-stu-id="10cf8-188">ABRed</span></span></li>
<li><span data-ttu-id="10cf8-189">ABRedComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-189">ABRedComposited</span></span></li>
<li><span data-ttu-id="10cf8-190">ABYellow</span><span class="sxs-lookup"><span data-stu-id="10cf8-190">ABYellow</span></span></li>
<li><span data-ttu-id="10cf8-191">ABYellowComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-191">ABYellowComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10cf8-192">SearchBox</span><span class="sxs-lookup"><span data-stu-id="10cf8-192">SearchBox</span></span></td>
<td><ul>
<li><span data-ttu-id="10cf8-193">InactiveSearchBox</span><span class="sxs-lookup"><span data-stu-id="10cf8-193">InactiveSearchBox</span></span></li>
<li><span data-ttu-id="10cf8-194">InactiveSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-194">InactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="10cf8-195">MaxInactiveSearchBox</span><span class="sxs-lookup"><span data-stu-id="10cf8-195">MaxInactiveSearchBox</span></span></li>
<li><span data-ttu-id="10cf8-196">MaxInactiveSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-196">MaxInactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="10cf8-197">MaxSearchBox</span><span class="sxs-lookup"><span data-stu-id="10cf8-197">MaxSearchBox</span></span></li>
<li><span data-ttu-id="10cf8-198">MaxSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-198">MaxSearchBoxComposited</span></span></li>
<li><span data-ttu-id="10cf8-199">SearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="10cf8-199">SearchBoxComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="10cf8-200">En la tabla siguiente se muestran los detalles de estas clases.</span><span class="sxs-lookup"><span data-stu-id="10cf8-200">The following table shows the specifics of these classes.</span></span>



| <span data-ttu-id="10cf8-201">Control</span><span class="sxs-lookup"><span data-stu-id="10cf8-201">Control</span></span>     | <span data-ttu-id="10cf8-202">Parte</span><span class="sxs-lookup"><span data-stu-id="10cf8-202">Part</span></span>         | <span data-ttu-id="10cf8-203">States</span><span class="sxs-lookup"><span data-stu-id="10cf8-203">States</span></span>                                                 |
|-------------|--------------|--------------------------------------------------------|
| <span data-ttu-id="10cf8-204">ADDRESSBAND</span><span class="sxs-lookup"><span data-stu-id="10cf8-204">ADDRESSBAND</span></span> | <span data-ttu-id="10cf8-205">ABBACKGROUND</span><span class="sxs-lookup"><span data-stu-id="10cf8-205">ABBACKGROUND</span></span> | <span data-ttu-id="10cf8-206">NORMAL (0x1), activo (0X2), deshabilitado (0X3), centrado (0x4)</span><span class="sxs-lookup"><span data-stu-id="10cf8-206">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |
| <span data-ttu-id="10cf8-207">CONTROL SEARCHBOX</span><span class="sxs-lookup"><span data-stu-id="10cf8-207">SEARCHBOX</span></span>   | <span data-ttu-id="10cf8-208">SBBACKGROUND</span><span class="sxs-lookup"><span data-stu-id="10cf8-208">SBBACKGROUND</span></span> | <span data-ttu-id="10cf8-209">NORMAL (0x1), activo (0X2), deshabilitado (0X3), centrado (0x4)</span><span class="sxs-lookup"><span data-stu-id="10cf8-209">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |



 

 

 




