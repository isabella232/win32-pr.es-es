---
title: Otros roles de objeto y métodos admitidos (referencia de elementos de interfaz de usuario de MSAA)
description: En este tema se proporciona información sobre los roles de objeto que no se incluyen en los temas anteriores de los elementos de la interfaz de usuario.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3d7fbdbb6dfbf83729f3e1c1d4caa3027f8d51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792921"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="3cbec-103">Otros roles de objeto y métodos admitidos (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="3cbec-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="3cbec-104">En este tema se proporciona información sobre los roles de objeto que no se incluyen en los temas anteriores de los elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3cbec-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="3cbec-105">Cada rol de objeto incluye una lista de los métodos y propiedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que se admiten para el rol de objeto.</span><span class="sxs-lookup"><span data-stu-id="3cbec-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="3cbec-106">Mientras que otros temas documentan los métodos y propiedades de **IAccessible** compatibles con los elementos de la interfaz de usuario, en este tema se enumeran los métodos y las propiedades que puede esperar que se admitan para un rol de objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="3cbec-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="3cbec-107">Muchos de los elementos de la interfaz de usuario que pueden tener uno de los roles enumerados aquí se suelen ver en los exploradores.</span><span class="sxs-lookup"><span data-stu-id="3cbec-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="3cbec-108">Use este tema como guía.</span><span class="sxs-lookup"><span data-stu-id="3cbec-108">Use this topic as a guideline.</span></span> <span data-ttu-id="3cbec-109">Le recomendamos encarecidamente que use herramientas de Active Accessibility de Microsoft para comprobar el comportamiento esperado de un rol de objeto individual.</span><span class="sxs-lookup"><span data-stu-id="3cbec-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="3cbec-110">En la tabla siguiente se enumeran los roles de objeto adicionales que admite Oleacc.dll.</span><span class="sxs-lookup"><span data-stu-id="3cbec-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



|                                                                         |                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="3cbec-111">**\_alerta del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="3cbec-112">**desplegable sistema de roles \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="3cbec-113">**\_aplicación de sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="3cbec-114">**\_ecuación del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="3cbec-115">**\_borde del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="3cbec-116">**\_gráfico del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="3cbec-117">**\_BUTTONDROPDOWN del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="3cbec-118">**\_HELPBALLOON del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="3cbec-119">**\_BUTTONDROPDOWNGRID del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="3cbec-120">**\_IPAddress del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="3cbec-121">**\_BUTTONMENU del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="3cbec-122">**\_vínculo del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="3cbec-123">**\_celda del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="3cbec-124">**\_panel del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="3cbec-125">**\_carácter de sistema de rol \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="3cbec-126">**\_fila del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="3cbec-127">**\_gráfico del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="3cbec-128">**\_ROWHEADER del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="3cbec-129">**\_reloj del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="3cbec-130">**separador de sistema de roles \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="3cbec-131">**\_columna del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="3cbec-132">**\_sonido del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="3cbec-133">**\_Diagrama del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="3cbec-134">**sistema de roles \_ \_ SPLITBUTTON**</span><span class="sxs-lookup"><span data-stu-id="3cbec-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="3cbec-135">**\_marcado del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="3cbec-136">**\_tabla del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="3cbec-137">**\_documento de sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="3cbec-138">**\_espacio en blanco del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="3cbec-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="3cbec-139">\_alerta del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="3cbec-140">Para obtener más información sobre este rol, [**consulte \_ \_ alerta del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-141">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-142">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-142">get\_accName</span></span>
-   <span data-ttu-id="3cbec-143">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-143">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-144">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="3cbec-145">\_aplicación de sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="3cbec-146">Para obtener más información sobre este rol, [**vea \_ \_ aplicación de sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-147">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-148">accHitTest</span></span>
-   <span data-ttu-id="3cbec-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-149">accLocation</span></span>
-   <span data-ttu-id="3cbec-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-150">accNavigate</span></span>
-   <span data-ttu-id="3cbec-151">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-151">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-152">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-152">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-153">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-153">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-154">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-154">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-155">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-156">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-157">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-157">get\_accName</span></span>
-   <span data-ttu-id="3cbec-158">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-158">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-159">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-159">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-160">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="3cbec-161">\_borde del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="3cbec-162">Para obtener más información sobre este rol, [**vea \_ \_ borde del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-163">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-164">accHitTest</span></span>
-   <span data-ttu-id="3cbec-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-165">accLocation</span></span>
-   <span data-ttu-id="3cbec-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-166">accNavigate</span></span>
-   <span data-ttu-id="3cbec-167">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-167">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-168">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="3cbec-169">\_BUTTONDROPDOWN del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="3cbec-170">Para obtener más información sobre este rol, [**consulte \_ \_ BUTTONDROPDOWN de sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-171">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="3cbec-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-173">accHitTest</span></span>
-   <span data-ttu-id="3cbec-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-174">accLocation</span></span>
-   <span data-ttu-id="3cbec-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-175">accNavigate</span></span>
-   <span data-ttu-id="3cbec-176">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-176">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-177">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-177">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-178">obtener \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="3cbec-179">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-179">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-180">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-180">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-181">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-182">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-183">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-183">get\_accName</span></span>
-   <span data-ttu-id="3cbec-184">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-184">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-185">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-185">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-186">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="3cbec-187">\_BUTTONDROPDOWNGRID del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="3cbec-188">Para obtener más información sobre este rol, [**consulte \_ \_ BUTTONDROPDOWNGRID de sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-189">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="3cbec-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-191">accHitTest</span></span>
-   <span data-ttu-id="3cbec-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-192">accLocation</span></span>
-   <span data-ttu-id="3cbec-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-193">accNavigate</span></span>
-   <span data-ttu-id="3cbec-194">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-194">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-195">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-195">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-196">obtener \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="3cbec-197">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-197">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-198">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-198">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-199">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-200">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-201">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-201">get\_accName</span></span>
-   <span data-ttu-id="3cbec-202">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-202">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-203">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-203">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-204">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="3cbec-205">\_BUTTONMENU del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="3cbec-206">Para obtener más información sobre este rol, vea el caso de la función [**\_ \_ BUTTONMENU del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-207">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-208">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="3cbec-209">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-209">accHitTest</span></span>
-   <span data-ttu-id="3cbec-210">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-210">accLocation</span></span>
-   <span data-ttu-id="3cbec-211">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-211">accNavigate</span></span>
-   <span data-ttu-id="3cbec-212">obtener \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="3cbec-213">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-213">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-214">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-214">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-215">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-216">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-217">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-217">get\_accName</span></span>
-   <span data-ttu-id="3cbec-218">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-218">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-219">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-219">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-220">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="3cbec-221">\_celda del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="3cbec-222">Para obtener más información sobre este rol, [**consulte \_ \_ celda del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-223">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-224">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-224">accHitTest</span></span>
-   <span data-ttu-id="3cbec-225">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-225">accLocation</span></span>
-   <span data-ttu-id="3cbec-226">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-226">accNavigate</span></span>
-   <span data-ttu-id="3cbec-227">accSelect</span><span class="sxs-lookup"><span data-stu-id="3cbec-227">accSelect</span></span>
-   <span data-ttu-id="3cbec-228">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-228">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-229">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-229">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-230">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-230">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-231">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-231">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-232">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-233">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-234">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-234">get\_accName</span></span>
-   <span data-ttu-id="3cbec-235">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-235">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-236">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-236">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-237">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-237">get\_accState</span></span>
-   <span data-ttu-id="3cbec-238">obtener \_ accValue</span><span class="sxs-lookup"><span data-stu-id="3cbec-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="3cbec-239">\_carácter de sistema de rol \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="3cbec-240">Para obtener más información sobre este rol, [**vea \_ \_ carácter de sistema de rol**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-241">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-242">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-242">accHitTest</span></span>
-   <span data-ttu-id="3cbec-243">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-243">accLocation</span></span>
-   <span data-ttu-id="3cbec-244">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-244">accNavigate</span></span>
-   <span data-ttu-id="3cbec-245">obtener \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="3cbec-245">get\_accDescription</span></span>
-   <span data-ttu-id="3cbec-246">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-246">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-247">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-248">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-248">get\_accName</span></span>
-   <span data-ttu-id="3cbec-249">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-249">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-250">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-250">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-251">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-251">get\_accState</span></span>
-   <span data-ttu-id="3cbec-252">obtener \_ accValue</span><span class="sxs-lookup"><span data-stu-id="3cbec-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="3cbec-253">\_gráfico del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="3cbec-254">Para más información sobre este rol, consulte [**el \_ \_ gráfico del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-255">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-256">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-256">accHitTest</span></span>
-   <span data-ttu-id="3cbec-257">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-257">accLocation</span></span>
-   <span data-ttu-id="3cbec-258">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-258">accNavigate</span></span>
-   <span data-ttu-id="3cbec-259">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-259">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-260">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-260">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-261">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-261">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-262">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-262">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-263">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-264">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-265">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-265">get\_accName</span></span>
-   <span data-ttu-id="3cbec-266">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-266">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-267">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-267">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-268">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="3cbec-269">\_reloj del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="3cbec-270">Para obtener más información sobre este rol, consulte el [**\_ \_ reloj del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-271">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-272">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-272">accHitTest</span></span>
-   <span data-ttu-id="3cbec-273">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-273">accLocation</span></span>
-   <span data-ttu-id="3cbec-274">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-274">accNavigate</span></span>
-   <span data-ttu-id="3cbec-275">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-275">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-276">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-276">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-277">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-278">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-279">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-279">get\_accName</span></span>
-   <span data-ttu-id="3cbec-280">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-280">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-281">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-281">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-282">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-282">get\_accState</span></span>
-   <span data-ttu-id="3cbec-283">obtener \_ accValue</span><span class="sxs-lookup"><span data-stu-id="3cbec-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="3cbec-284">\_columna del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="3cbec-285">Para obtener más información sobre este rol, consulte la [**\_ \_ columna sistema de rol**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-286">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-287">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-287">accHitTest</span></span>
-   <span data-ttu-id="3cbec-288">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-288">accLocation</span></span>
-   <span data-ttu-id="3cbec-289">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-289">accNavigate</span></span>
-   <span data-ttu-id="3cbec-290">accSelect</span><span class="sxs-lookup"><span data-stu-id="3cbec-290">accSelect</span></span>
-   <span data-ttu-id="3cbec-291">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-291">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-292">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-292">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-293">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-293">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-294">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-294">get\_accName</span></span>
-   <span data-ttu-id="3cbec-295">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-295">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-296">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-296">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-297">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-297">get\_accState</span></span>
-   <span data-ttu-id="3cbec-298">obtener \_ accValue</span><span class="sxs-lookup"><span data-stu-id="3cbec-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="3cbec-299">\_Diagrama del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="3cbec-300">Para obtener más información sobre este rol, [**vea \_ \_ Diagrama de sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-301">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-302">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-302">accHitTest</span></span>
-   <span data-ttu-id="3cbec-303">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-303">accLocation</span></span>
-   <span data-ttu-id="3cbec-304">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-304">accNavigate</span></span>
-   <span data-ttu-id="3cbec-305">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-305">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-306">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-306">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-307">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-307">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-308">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-308">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-309">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-310">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-311">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-311">get\_accName</span></span>
-   <span data-ttu-id="3cbec-312">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-312">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-313">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-313">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-314">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="3cbec-315">\_marcado del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="3cbec-316">Para obtener más información sobre este rol, [**consulte \_ \_ marcado del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-317">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-318">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="3cbec-319">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-319">accHitTest</span></span>
-   <span data-ttu-id="3cbec-320">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-320">accLocation</span></span>
-   <span data-ttu-id="3cbec-321">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-321">accNavigate</span></span>
-   <span data-ttu-id="3cbec-322">obtener \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="3cbec-323">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-323">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-324">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-324">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-325">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-326">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-327">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-327">get\_accName</span></span>
-   <span data-ttu-id="3cbec-328">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-328">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-329">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-329">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-330">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-330">get\_accState</span></span>
-   <span data-ttu-id="3cbec-331">obtener \_ accValue</span><span class="sxs-lookup"><span data-stu-id="3cbec-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="3cbec-332">\_documento de sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="3cbec-333">Para obtener más información sobre este rol, consulte el [**\_ \_ documento**](object-roles.md)sobre el sistema de roles.</span><span class="sxs-lookup"><span data-stu-id="3cbec-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-334">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-335">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-335">accHitTest</span></span>
-   <span data-ttu-id="3cbec-336">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-336">accLocation</span></span>
-   <span data-ttu-id="3cbec-337">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-337">accNavigate</span></span>
-   <span data-ttu-id="3cbec-338">accSelect</span><span class="sxs-lookup"><span data-stu-id="3cbec-338">accSelect</span></span>
-   <span data-ttu-id="3cbec-339">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-339">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-340">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-340">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-341">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-341">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-342">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-342">get\_accName</span></span>
-   <span data-ttu-id="3cbec-343">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-343">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-344">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-344">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-345">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="3cbec-346">desplegable sistema de roles \_ \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="3cbec-347">Para obtener más información sobre este rol, vea el apartado de la [**\_ \_ desplegable del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-348">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-349">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="3cbec-350">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-350">accHitTest</span></span>
-   <span data-ttu-id="3cbec-351">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-351">accLocation</span></span>
-   <span data-ttu-id="3cbec-352">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-352">accNavigate</span></span>
-   <span data-ttu-id="3cbec-353">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-353">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-354">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-354">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-355">obtener \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="3cbec-356">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-356">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-357">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-357">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-358">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-359">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-360">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-360">get\_accName</span></span>
-   <span data-ttu-id="3cbec-361">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-361">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-362">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-362">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-363">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="3cbec-364">\_ecuación del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="3cbec-365">Para obtener más información sobre este rol, [**vea \_ \_ ecuación del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-366">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-367">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-367">accHitTest</span></span>
-   <span data-ttu-id="3cbec-368">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-368">accLocation</span></span>
-   <span data-ttu-id="3cbec-369">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-369">accNavigate</span></span>
-   <span data-ttu-id="3cbec-370">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-370">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-371">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-371">get\_accName</span></span>
-   <span data-ttu-id="3cbec-372">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-372">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-373">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-373">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-374">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-374">get\_accState</span></span>
-   <span data-ttu-id="3cbec-375">obtener \_ accValue</span><span class="sxs-lookup"><span data-stu-id="3cbec-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="3cbec-376">\_gráfico del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="3cbec-377">Para obtener más información sobre este rol, consulte el [**\_ \_ gráfico del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-378">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-379">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-379">accHitTest</span></span>
-   <span data-ttu-id="3cbec-380">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-380">accLocation</span></span>
-   <span data-ttu-id="3cbec-381">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-381">accNavigate</span></span>
-   <span data-ttu-id="3cbec-382">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-382">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-383">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-383">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-384">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-385">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-386">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-386">get\_accName</span></span>
-   <span data-ttu-id="3cbec-387">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-387">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-388">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-388">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-389">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="3cbec-390">\_HELPBALLOON del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="3cbec-391">Para obtener más información sobre este rol, [**consulte \_ \_ HELPBALLOON de sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-392">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-393">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-393">accHitTest</span></span>
-   <span data-ttu-id="3cbec-394">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-394">accLocation</span></span>
-   <span data-ttu-id="3cbec-395">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-395">accNavigate</span></span>
-   <span data-ttu-id="3cbec-396">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-396">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-397">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-397">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-398">obtener \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="3cbec-399">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-399">get\_accName</span></span>
-   <span data-ttu-id="3cbec-400">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-400">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-401">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-401">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-402">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-402">get\_accState</span></span>
-   <span data-ttu-id="3cbec-403">obtener \_ accValue</span><span class="sxs-lookup"><span data-stu-id="3cbec-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="3cbec-404">\_IPAddress del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="3cbec-405">Para obtener más información sobre este rol, [**consulte \_ \_ IPAddress del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-406">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-407">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-407">accHitTest</span></span>
-   <span data-ttu-id="3cbec-408">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-408">accLocation</span></span>
-   <span data-ttu-id="3cbec-409">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-409">accNavigate</span></span>
-   <span data-ttu-id="3cbec-410">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-410">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-411">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-411">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-412">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-412">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-413">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-413">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-414">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-415">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-416">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-416">get\_accName</span></span>
-   <span data-ttu-id="3cbec-417">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-417">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-418">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-418">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-419">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-419">get\_accState</span></span>
-   <span data-ttu-id="3cbec-420">obtener \_ accValue</span><span class="sxs-lookup"><span data-stu-id="3cbec-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="3cbec-421">\_vínculo del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="3cbec-422">Para obtener más información sobre este rol, [**consulte \_ \_ vínculo del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-423">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-424">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="3cbec-425">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-425">accHitTest</span></span>
-   <span data-ttu-id="3cbec-426">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-426">accLocation</span></span>
-   <span data-ttu-id="3cbec-427">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-427">accNavigate</span></span>
-   <span data-ttu-id="3cbec-428">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-428">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-429">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-429">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-430">obtener \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="3cbec-431">obtener \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="3cbec-431">get\_accDescription</span></span>
-   <span data-ttu-id="3cbec-432">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-432">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-433">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-434">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-434">get\_accName</span></span>
-   <span data-ttu-id="3cbec-435">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-435">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-436">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-436">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-437">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-437">get\_accState</span></span>
-   <span data-ttu-id="3cbec-438">obtener \_ accValue</span><span class="sxs-lookup"><span data-stu-id="3cbec-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="3cbec-439">\_panel del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="3cbec-440">Para obtener más información sobre este rol, [**consulte \_ \_ panel del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-441">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-442">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-442">accHitTest</span></span>
-   <span data-ttu-id="3cbec-443">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-443">accLocation</span></span>
-   <span data-ttu-id="3cbec-444">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-444">accNavigate</span></span>
-   <span data-ttu-id="3cbec-445">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-445">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-446">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-446">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-447">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-447">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-448">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-448">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-449">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-450">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-451">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-451">get\_accName</span></span>
-   <span data-ttu-id="3cbec-452">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-452">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-453">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-453">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-454">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="3cbec-455">\_fila del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="3cbec-456">Para obtener más información sobre este rol, vea rol de la [**\_ \_ fila de sistema**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-457">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-458">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-458">accHitTest</span></span>
-   <span data-ttu-id="3cbec-459">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-459">accLocation</span></span>
-   <span data-ttu-id="3cbec-460">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-460">accNavigate</span></span>
-   <span data-ttu-id="3cbec-461">accSelect</span><span class="sxs-lookup"><span data-stu-id="3cbec-461">accSelect</span></span>
-   <span data-ttu-id="3cbec-462">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-462">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-463">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-463">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-464">obtener \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="3cbec-464">get\_accDescription</span></span>
-   <span data-ttu-id="3cbec-465">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-465">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-466">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-466">get\_accName</span></span>
-   <span data-ttu-id="3cbec-467">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-467">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-468">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-468">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-469">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-469">get\_accState</span></span>
-   <span data-ttu-id="3cbec-470">obtener \_ accValue</span><span class="sxs-lookup"><span data-stu-id="3cbec-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="3cbec-471">\_ROWHEADER del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="3cbec-472">Para obtener más información sobre este rol, [**consulte \_ \_ ROWHEADER de sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-473">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-474">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-474">accHitTest</span></span>
-   <span data-ttu-id="3cbec-475">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-475">accLocation</span></span>
-   <span data-ttu-id="3cbec-476">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-476">accNavigate</span></span>
-   <span data-ttu-id="3cbec-477">accSelect</span><span class="sxs-lookup"><span data-stu-id="3cbec-477">accSelect</span></span>
-   <span data-ttu-id="3cbec-478">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-478">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-479">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-479">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-480">obtener \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="3cbec-481">obtener \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="3cbec-481">get\_accDescription</span></span>
-   <span data-ttu-id="3cbec-482">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-482">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-483">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-483">get\_accName</span></span>
-   <span data-ttu-id="3cbec-484">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-484">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-485">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-485">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-486">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-486">get\_accState</span></span>
-   <span data-ttu-id="3cbec-487">obtener \_ accValue</span><span class="sxs-lookup"><span data-stu-id="3cbec-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="3cbec-488">separador de sistema de roles \_ \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="3cbec-489">Para obtener más información sobre este rol, [**consulte \_ \_ separador de sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-490">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-491">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-491">accHitTest</span></span>
-   <span data-ttu-id="3cbec-492">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-492">accLocation</span></span>
-   <span data-ttu-id="3cbec-493">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-493">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-494">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-494">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-495">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-495">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-496">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-496">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-497">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="3cbec-498">\_sonido del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="3cbec-499">Para obtener más información sobre este rol, [**vea \_ \_ sonido del sistema de funciones**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-500">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-501">obtener \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="3cbec-501">get\_accDescription</span></span>
-   <span data-ttu-id="3cbec-502">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-502">get\_accName</span></span>
-   <span data-ttu-id="3cbec-503">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-503">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-504">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="3cbec-505">sistema de roles \_ \_ SPLITBUTTON</span><span class="sxs-lookup"><span data-stu-id="3cbec-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="3cbec-506">Para obtener más información sobre este rol, vea [**rol \_ System \_ SPLITBUTTON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-507">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="3cbec-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-509">accHitTest</span></span>
-   <span data-ttu-id="3cbec-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-510">accLocation</span></span>
-   <span data-ttu-id="3cbec-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-511">accNavigate</span></span>
-   <span data-ttu-id="3cbec-512">obtener \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="3cbec-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="3cbec-513">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-513">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-514">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-515">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-516">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-516">get\_accName</span></span>
-   <span data-ttu-id="3cbec-517">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-517">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-518">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-518">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-519">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="3cbec-520">\_tabla del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="3cbec-521">Para obtener más información sobre este rol, [**consulte \_ \_ tabla del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-522">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="3cbec-523">accHitTest</span></span>
-   <span data-ttu-id="3cbec-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-524">accLocation</span></span>
-   <span data-ttu-id="3cbec-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="3cbec-525">accNavigate</span></span>
-   <span data-ttu-id="3cbec-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="3cbec-526">accSelect</span></span>
-   <span data-ttu-id="3cbec-527">obtener \_ accChild</span><span class="sxs-lookup"><span data-stu-id="3cbec-527">get\_accChild</span></span>
-   <span data-ttu-id="3cbec-528">obtener \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="3cbec-528">get\_accChildCount</span></span>
-   <span data-ttu-id="3cbec-529">obtener \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="3cbec-529">get\_accDescription</span></span>
-   <span data-ttu-id="3cbec-530">obtener \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="3cbec-530">get\_accFocus</span></span>
-   <span data-ttu-id="3cbec-531">obtener \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="3cbec-531">get\_accHelp</span></span>
-   <span data-ttu-id="3cbec-532">obtener \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="3cbec-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="3cbec-533">obtener \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3cbec-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="3cbec-534">obtener \_ accName</span><span class="sxs-lookup"><span data-stu-id="3cbec-534">get\_accName</span></span>
-   <span data-ttu-id="3cbec-535">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-535">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-536">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-536">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-537">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="3cbec-538">\_espacio en blanco del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="3cbec-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="3cbec-539">Para obtener más información sobre este rol, [**vea \_ \_ espacio en blanco del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3cbec-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="3cbec-540">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="3cbec-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="3cbec-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="3cbec-541">accLocation</span></span>
-   <span data-ttu-id="3cbec-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="3cbec-542">accSelect</span></span>
-   <span data-ttu-id="3cbec-543">obtener \_ accParent</span><span class="sxs-lookup"><span data-stu-id="3cbec-543">get\_accParent</span></span>
-   <span data-ttu-id="3cbec-544">obtener \_ accRole</span><span class="sxs-lookup"><span data-stu-id="3cbec-544">get\_accRole</span></span>
-   <span data-ttu-id="3cbec-545">obtener \_ accState</span><span class="sxs-lookup"><span data-stu-id="3cbec-545">get\_accState</span></span>

 

 