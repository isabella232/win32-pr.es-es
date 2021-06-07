---
title: Otros roles de objeto y métodos admitidos (Referencia de elementos de la interfaz de usuario de MSAA)
description: En este tema se proporciona información sobre los roles de objeto que no se incluyen en los temas anteriores para los elementos de la interfaz de usuario.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17e8573142a57e0acf08980895fdae3ea6d1841
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444006"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="386e2-103">Otros roles de objeto y métodos admitidos (Referencia de elementos de la interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="386e2-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="386e2-104">En este tema se proporciona información sobre los roles de objeto que no se incluyen en los temas anteriores para los elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="386e2-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="386e2-105">Cada rol de objeto incluye una lista de los métodos y propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que se admiten para el rol de objeto.</span><span class="sxs-lookup"><span data-stu-id="386e2-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="386e2-106">Aunque otros temas documentan propiedades y métodos **IAccessible** admitidos para los elementos de la interfaz de usuario, en este tema se enumeran los métodos y propiedades que puede esperar que se admiten para un rol de objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="386e2-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="386e2-107">Muchos de los elementos de la interfaz de usuario que podrían tener uno de los roles enumerados aquí se suelen ver en los exploradores.</span><span class="sxs-lookup"><span data-stu-id="386e2-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="386e2-108">Use este tema como guía.</span><span class="sxs-lookup"><span data-stu-id="386e2-108">Use this topic as a guideline.</span></span> <span data-ttu-id="386e2-109">Se recomienda encarecidamente usar herramientas de Microsoft Active Accessibility para comprobar el comportamiento esperado de un rol de objeto individual.</span><span class="sxs-lookup"><span data-stu-id="386e2-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="386e2-110">En la tabla siguiente se enumeran los roles de objeto adicionales que Oleacc.dll admite.</span><span class="sxs-lookup"><span data-stu-id="386e2-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



| &nbsp; |  &nbsp; |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="386e2-111">**ALERTA \_ DEL SISTEMA DE \_ ROL**</span><span class="sxs-lookup"><span data-stu-id="386e2-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="386e2-112">**LISTA DESPLEGABLE \_ DEL \_ SISTEMA DE ROL**</span><span class="sxs-lookup"><span data-stu-id="386e2-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="386e2-113">**APLICACIÓN \_ DEL SISTEMA DE \_ ROLES**</span><span class="sxs-lookup"><span data-stu-id="386e2-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="386e2-114">**ECUACIÓN \_ DEL SISTEMA \_ DE ROL**</span><span class="sxs-lookup"><span data-stu-id="386e2-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="386e2-115">**BORDE \_ DEL SISTEMA DE \_ ROL**</span><span class="sxs-lookup"><span data-stu-id="386e2-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="386e2-116">**GRÁFICO \_ DEL SISTEMA DE \_ ROLES**</span><span class="sxs-lookup"><span data-stu-id="386e2-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="386e2-117">**ROLE \_ SYSTEM \_ BUTTONDROPDOWN**</span><span class="sxs-lookup"><span data-stu-id="386e2-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="386e2-118">**ROLE \_ SYSTEM \_ HELPBALLOON**</span><span class="sxs-lookup"><span data-stu-id="386e2-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="386e2-119">**ROLE \_ SYSTEM \_ BUTTONDROPDOWNGRID**</span><span class="sxs-lookup"><span data-stu-id="386e2-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="386e2-120">**ROLE \_ SYSTEM \_ IPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="386e2-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="386e2-121">**ROLE \_ SYSTEM \_ BUTTONMENU**</span><span class="sxs-lookup"><span data-stu-id="386e2-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="386e2-122">**VÍNCULO \_ DEL SISTEMA DE \_ ROLES**</span><span class="sxs-lookup"><span data-stu-id="386e2-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="386e2-123">**CELDA \_ DEL SISTEMA DE \_ ROL**</span><span class="sxs-lookup"><span data-stu-id="386e2-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="386e2-124">**PANEL \_ SISTEMA DE \_ ROL**</span><span class="sxs-lookup"><span data-stu-id="386e2-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="386e2-125">**CARÁCTER \_ DEL SISTEMA DE \_ ROLES**</span><span class="sxs-lookup"><span data-stu-id="386e2-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="386e2-126">**FILA \_ DEL SISTEMA DE \_ ROL**</span><span class="sxs-lookup"><span data-stu-id="386e2-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="386e2-127">**GRÁFICO \_ DEL SISTEMA DE \_ ROLES**</span><span class="sxs-lookup"><span data-stu-id="386e2-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="386e2-128">**ROLE \_ SYSTEM \_ ROWHEADER**</span><span class="sxs-lookup"><span data-stu-id="386e2-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="386e2-129">**RELOJ \_ DEL SISTEMA DE \_ ROL**</span><span class="sxs-lookup"><span data-stu-id="386e2-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="386e2-130">**SEPARADOR \_ DEL SISTEMA DE \_ ROLES**</span><span class="sxs-lookup"><span data-stu-id="386e2-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="386e2-131">**COLUMNA \_ DEL SISTEMA DE \_ ROL**</span><span class="sxs-lookup"><span data-stu-id="386e2-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="386e2-132">**SONIDO \_ DEL SISTEMA DE \_ ROL**</span><span class="sxs-lookup"><span data-stu-id="386e2-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="386e2-133">**DIAGRAMA \_ DEL SISTEMA DE \_ ROLES**</span><span class="sxs-lookup"><span data-stu-id="386e2-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="386e2-134">**ROLE \_ SYSTEM \_ SPLITBUTTON**</span><span class="sxs-lookup"><span data-stu-id="386e2-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="386e2-135">**MARCADO \_ DEL SISTEMA DE \_ ROL**</span><span class="sxs-lookup"><span data-stu-id="386e2-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="386e2-136">**TABLA \_ DEL SISTEMA DE \_ ROLES**</span><span class="sxs-lookup"><span data-stu-id="386e2-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="386e2-137">**DOCUMENTO \_ DEL SISTEMA DE \_ ROLES**</span><span class="sxs-lookup"><span data-stu-id="386e2-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="386e2-138">**ESPACIO \_ EN BLANCO DEL SISTEMA DE \_ ROLES**</span><span class="sxs-lookup"><span data-stu-id="386e2-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="386e2-139">ALERTA \_ DEL SISTEMA DE \_ ROL</span><span class="sxs-lookup"><span data-stu-id="386e2-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="386e2-140">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ ALERT**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="386e2-141">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-142">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-142">get\_accName</span></span>
-   <span data-ttu-id="386e2-143">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-143">get\_accRole</span></span>
-   <span data-ttu-id="386e2-144">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="386e2-145">APLICACIÓN \_ DEL SISTEMA DE \_ ROLES</span><span class="sxs-lookup"><span data-stu-id="386e2-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="386e2-146">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ APPLICATION**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="386e2-147">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-148">accHitTest</span></span>
-   <span data-ttu-id="386e2-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-149">accLocation</span></span>
-   <span data-ttu-id="386e2-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-150">accNavigate</span></span>
-   <span data-ttu-id="386e2-151">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-151">get\_accChild</span></span>
-   <span data-ttu-id="386e2-152">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-152">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-153">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-153">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-154">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-154">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-155">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-156">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-157">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-157">get\_accName</span></span>
-   <span data-ttu-id="386e2-158">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-158">get\_accParent</span></span>
-   <span data-ttu-id="386e2-159">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-159">get\_accRole</span></span>
-   <span data-ttu-id="386e2-160">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="386e2-161">BORDE \_ DEL SISTEMA DE \_ ROL</span><span class="sxs-lookup"><span data-stu-id="386e2-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="386e2-162">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ BORDER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="386e2-163">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-164">accHitTest</span></span>
-   <span data-ttu-id="386e2-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-165">accLocation</span></span>
-   <span data-ttu-id="386e2-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-166">accNavigate</span></span>
-   <span data-ttu-id="386e2-167">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-167">get\_accRole</span></span>
-   <span data-ttu-id="386e2-168">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="386e2-169">ROLE \_ SYSTEM \_ BUTTONDROPDOWN</span><span class="sxs-lookup"><span data-stu-id="386e2-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="386e2-170">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ BUTTONDROPDOWN**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="386e2-171">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="386e2-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-173">accHitTest</span></span>
-   <span data-ttu-id="386e2-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-174">accLocation</span></span>
-   <span data-ttu-id="386e2-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-175">accNavigate</span></span>
-   <span data-ttu-id="386e2-176">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-176">get\_accChild</span></span>
-   <span data-ttu-id="386e2-177">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-177">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-178">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="386e2-179">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-179">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-180">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-180">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-181">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-182">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-183">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-183">get\_accName</span></span>
-   <span data-ttu-id="386e2-184">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-184">get\_accParent</span></span>
-   <span data-ttu-id="386e2-185">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-185">get\_accRole</span></span>
-   <span data-ttu-id="386e2-186">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="386e2-187">ROLE \_ SYSTEM \_ BUTTONDROPDOWNGRID</span><span class="sxs-lookup"><span data-stu-id="386e2-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="386e2-188">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ BUTTONDROPDOWNGRID**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="386e2-189">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="386e2-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-191">accHitTest</span></span>
-   <span data-ttu-id="386e2-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-192">accLocation</span></span>
-   <span data-ttu-id="386e2-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-193">accNavigate</span></span>
-   <span data-ttu-id="386e2-194">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-194">get\_accChild</span></span>
-   <span data-ttu-id="386e2-195">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-195">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-196">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="386e2-197">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-197">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-198">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-198">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-199">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-200">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-201">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-201">get\_accName</span></span>
-   <span data-ttu-id="386e2-202">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-202">get\_accParent</span></span>
-   <span data-ttu-id="386e2-203">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-203">get\_accRole</span></span>
-   <span data-ttu-id="386e2-204">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="386e2-205">ROLE \_ SYSTEM \_ BUTTONMENU</span><span class="sxs-lookup"><span data-stu-id="386e2-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="386e2-206">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ BUTTONMENU**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="386e2-207">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-208">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="386e2-209">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-209">accHitTest</span></span>
-   <span data-ttu-id="386e2-210">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-210">accLocation</span></span>
-   <span data-ttu-id="386e2-211">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-211">accNavigate</span></span>
-   <span data-ttu-id="386e2-212">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="386e2-213">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-213">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-214">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-214">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-215">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-216">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-217">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-217">get\_accName</span></span>
-   <span data-ttu-id="386e2-218">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-218">get\_accParent</span></span>
-   <span data-ttu-id="386e2-219">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-219">get\_accRole</span></span>
-   <span data-ttu-id="386e2-220">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="386e2-221">CELDA \_ DEL SISTEMA DE \_ ROL</span><span class="sxs-lookup"><span data-stu-id="386e2-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="386e2-222">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ CELL**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="386e2-223">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-224">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-224">accHitTest</span></span>
-   <span data-ttu-id="386e2-225">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-225">accLocation</span></span>
-   <span data-ttu-id="386e2-226">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-226">accNavigate</span></span>
-   <span data-ttu-id="386e2-227">accSelect</span><span class="sxs-lookup"><span data-stu-id="386e2-227">accSelect</span></span>
-   <span data-ttu-id="386e2-228">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-228">get\_accChild</span></span>
-   <span data-ttu-id="386e2-229">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-229">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-230">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-230">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-231">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-231">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-232">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-233">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-234">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-234">get\_accName</span></span>
-   <span data-ttu-id="386e2-235">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-235">get\_accParent</span></span>
-   <span data-ttu-id="386e2-236">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-236">get\_accRole</span></span>
-   <span data-ttu-id="386e2-237">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-237">get\_accState</span></span>
-   <span data-ttu-id="386e2-238">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="386e2-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="386e2-239">CARÁCTER \_ DEL SISTEMA DE \_ ROLES</span><span class="sxs-lookup"><span data-stu-id="386e2-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="386e2-240">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ CHARACTER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="386e2-241">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-242">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-242">accHitTest</span></span>
-   <span data-ttu-id="386e2-243">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-243">accLocation</span></span>
-   <span data-ttu-id="386e2-244">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-244">accNavigate</span></span>
-   <span data-ttu-id="386e2-245">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="386e2-245">get\_accDescription</span></span>
-   <span data-ttu-id="386e2-246">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-246">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-247">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-248">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-248">get\_accName</span></span>
-   <span data-ttu-id="386e2-249">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-249">get\_accParent</span></span>
-   <span data-ttu-id="386e2-250">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-250">get\_accRole</span></span>
-   <span data-ttu-id="386e2-251">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-251">get\_accState</span></span>
-   <span data-ttu-id="386e2-252">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="386e2-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="386e2-253">GRÁFICO \_ DEL SISTEMA DE \_ ROLES</span><span class="sxs-lookup"><span data-stu-id="386e2-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="386e2-254">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ CHART**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="386e2-255">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-256">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-256">accHitTest</span></span>
-   <span data-ttu-id="386e2-257">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-257">accLocation</span></span>
-   <span data-ttu-id="386e2-258">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-258">accNavigate</span></span>
-   <span data-ttu-id="386e2-259">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-259">get\_accChild</span></span>
-   <span data-ttu-id="386e2-260">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-260">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-261">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-261">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-262">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-262">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-263">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-264">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-265">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-265">get\_accName</span></span>
-   <span data-ttu-id="386e2-266">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-266">get\_accParent</span></span>
-   <span data-ttu-id="386e2-267">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-267">get\_accRole</span></span>
-   <span data-ttu-id="386e2-268">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="386e2-269">RELOJ \_ DEL SISTEMA DE \_ ROL</span><span class="sxs-lookup"><span data-stu-id="386e2-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="386e2-270">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ CLOCK**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="386e2-271">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-272">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-272">accHitTest</span></span>
-   <span data-ttu-id="386e2-273">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-273">accLocation</span></span>
-   <span data-ttu-id="386e2-274">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-274">accNavigate</span></span>
-   <span data-ttu-id="386e2-275">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-275">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-276">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-276">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-277">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-278">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-279">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-279">get\_accName</span></span>
-   <span data-ttu-id="386e2-280">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-280">get\_accParent</span></span>
-   <span data-ttu-id="386e2-281">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-281">get\_accRole</span></span>
-   <span data-ttu-id="386e2-282">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-282">get\_accState</span></span>
-   <span data-ttu-id="386e2-283">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="386e2-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="386e2-284">COLUMNA \_ DEL SISTEMA DE \_ ROL</span><span class="sxs-lookup"><span data-stu-id="386e2-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="386e2-285">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ COLUMN**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="386e2-286">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-287">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-287">accHitTest</span></span>
-   <span data-ttu-id="386e2-288">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-288">accLocation</span></span>
-   <span data-ttu-id="386e2-289">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-289">accNavigate</span></span>
-   <span data-ttu-id="386e2-290">accSelect</span><span class="sxs-lookup"><span data-stu-id="386e2-290">accSelect</span></span>
-   <span data-ttu-id="386e2-291">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-291">get\_accChild</span></span>
-   <span data-ttu-id="386e2-292">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-292">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-293">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-293">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-294">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-294">get\_accName</span></span>
-   <span data-ttu-id="386e2-295">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-295">get\_accParent</span></span>
-   <span data-ttu-id="386e2-296">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-296">get\_accRole</span></span>
-   <span data-ttu-id="386e2-297">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-297">get\_accState</span></span>
-   <span data-ttu-id="386e2-298">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="386e2-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="386e2-299">DIAGRAMA \_ DEL SISTEMA DE \_ ROLES</span><span class="sxs-lookup"><span data-stu-id="386e2-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="386e2-300">Para obtener más información sobre este rol, vea [**DIAGRAMA DEL SISTEMA DE \_ \_ ROLES**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="386e2-301">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-302">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-302">accHitTest</span></span>
-   <span data-ttu-id="386e2-303">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-303">accLocation</span></span>
-   <span data-ttu-id="386e2-304">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-304">accNavigate</span></span>
-   <span data-ttu-id="386e2-305">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-305">get\_accChild</span></span>
-   <span data-ttu-id="386e2-306">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-306">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-307">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-307">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-308">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-308">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-309">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-310">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-311">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-311">get\_accName</span></span>
-   <span data-ttu-id="386e2-312">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-312">get\_accParent</span></span>
-   <span data-ttu-id="386e2-313">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-313">get\_accRole</span></span>
-   <span data-ttu-id="386e2-314">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="386e2-315">MARCADO \_ DEL SISTEMA DE \_ ROL</span><span class="sxs-lookup"><span data-stu-id="386e2-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="386e2-316">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ DIAL**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="386e2-317">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-318">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="386e2-319">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-319">accHitTest</span></span>
-   <span data-ttu-id="386e2-320">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-320">accLocation</span></span>
-   <span data-ttu-id="386e2-321">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-321">accNavigate</span></span>
-   <span data-ttu-id="386e2-322">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="386e2-323">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-323">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-324">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-324">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-325">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-326">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-327">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-327">get\_accName</span></span>
-   <span data-ttu-id="386e2-328">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-328">get\_accParent</span></span>
-   <span data-ttu-id="386e2-329">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-329">get\_accRole</span></span>
-   <span data-ttu-id="386e2-330">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-330">get\_accState</span></span>
-   <span data-ttu-id="386e2-331">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="386e2-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="386e2-332">DOCUMENTO \_ DEL SISTEMA DE \_ ROLES</span><span class="sxs-lookup"><span data-stu-id="386e2-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="386e2-333">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ DOCUMENT**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="386e2-334">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-335">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-335">accHitTest</span></span>
-   <span data-ttu-id="386e2-336">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-336">accLocation</span></span>
-   <span data-ttu-id="386e2-337">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-337">accNavigate</span></span>
-   <span data-ttu-id="386e2-338">accSelect</span><span class="sxs-lookup"><span data-stu-id="386e2-338">accSelect</span></span>
-   <span data-ttu-id="386e2-339">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-339">get\_accChild</span></span>
-   <span data-ttu-id="386e2-340">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-340">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-341">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-341">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-342">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-342">get\_accName</span></span>
-   <span data-ttu-id="386e2-343">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-343">get\_accParent</span></span>
-   <span data-ttu-id="386e2-344">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-344">get\_accRole</span></span>
-   <span data-ttu-id="386e2-345">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="386e2-346">LISTA DESPLEGABLE \_ DEL \_ SISTEMA DE ROL</span><span class="sxs-lookup"><span data-stu-id="386e2-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="386e2-347">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ DROPLIST**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="386e2-348">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-349">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="386e2-350">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-350">accHitTest</span></span>
-   <span data-ttu-id="386e2-351">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-351">accLocation</span></span>
-   <span data-ttu-id="386e2-352">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-352">accNavigate</span></span>
-   <span data-ttu-id="386e2-353">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-353">get\_accChild</span></span>
-   <span data-ttu-id="386e2-354">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-354">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-355">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="386e2-356">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-356">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-357">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-357">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-358">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-359">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-360">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-360">get\_accName</span></span>
-   <span data-ttu-id="386e2-361">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-361">get\_accParent</span></span>
-   <span data-ttu-id="386e2-362">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-362">get\_accRole</span></span>
-   <span data-ttu-id="386e2-363">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="386e2-364">ECUACIÓN \_ DEL SISTEMA \_ DE ROL</span><span class="sxs-lookup"><span data-stu-id="386e2-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="386e2-365">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ EQUATION**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="386e2-366">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-367">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-367">accHitTest</span></span>
-   <span data-ttu-id="386e2-368">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-368">accLocation</span></span>
-   <span data-ttu-id="386e2-369">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-369">accNavigate</span></span>
-   <span data-ttu-id="386e2-370">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-370">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-371">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-371">get\_accName</span></span>
-   <span data-ttu-id="386e2-372">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-372">get\_accParent</span></span>
-   <span data-ttu-id="386e2-373">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-373">get\_accRole</span></span>
-   <span data-ttu-id="386e2-374">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-374">get\_accState</span></span>
-   <span data-ttu-id="386e2-375">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="386e2-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="386e2-376">GRÁFICO \_ DEL SISTEMA DE \_ ROLES</span><span class="sxs-lookup"><span data-stu-id="386e2-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="386e2-377">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ GRAPHIC**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="386e2-378">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-379">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-379">accHitTest</span></span>
-   <span data-ttu-id="386e2-380">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-380">accLocation</span></span>
-   <span data-ttu-id="386e2-381">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-381">accNavigate</span></span>
-   <span data-ttu-id="386e2-382">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-382">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-383">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-383">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-384">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-385">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-386">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-386">get\_accName</span></span>
-   <span data-ttu-id="386e2-387">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-387">get\_accParent</span></span>
-   <span data-ttu-id="386e2-388">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-388">get\_accRole</span></span>
-   <span data-ttu-id="386e2-389">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="386e2-390">ROLE \_ SYSTEM \_ HELPBALLOON</span><span class="sxs-lookup"><span data-stu-id="386e2-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="386e2-391">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ HELPBALLOON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="386e2-392">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-393">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-393">accHitTest</span></span>
-   <span data-ttu-id="386e2-394">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-394">accLocation</span></span>
-   <span data-ttu-id="386e2-395">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-395">accNavigate</span></span>
-   <span data-ttu-id="386e2-396">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-396">get\_accChild</span></span>
-   <span data-ttu-id="386e2-397">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-397">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-398">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="386e2-399">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-399">get\_accName</span></span>
-   <span data-ttu-id="386e2-400">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-400">get\_accParent</span></span>
-   <span data-ttu-id="386e2-401">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-401">get\_accRole</span></span>
-   <span data-ttu-id="386e2-402">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-402">get\_accState</span></span>
-   <span data-ttu-id="386e2-403">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="386e2-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="386e2-404">ROLE \_ SYSTEM \_ IPADDRESS</span><span class="sxs-lookup"><span data-stu-id="386e2-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="386e2-405">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ IPADDRESS**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="386e2-406">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-407">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-407">accHitTest</span></span>
-   <span data-ttu-id="386e2-408">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-408">accLocation</span></span>
-   <span data-ttu-id="386e2-409">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-409">accNavigate</span></span>
-   <span data-ttu-id="386e2-410">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-410">get\_accChild</span></span>
-   <span data-ttu-id="386e2-411">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-411">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-412">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-412">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-413">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-413">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-414">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-415">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-416">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-416">get\_accName</span></span>
-   <span data-ttu-id="386e2-417">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-417">get\_accParent</span></span>
-   <span data-ttu-id="386e2-418">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-418">get\_accRole</span></span>
-   <span data-ttu-id="386e2-419">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-419">get\_accState</span></span>
-   <span data-ttu-id="386e2-420">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="386e2-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="386e2-421">VÍNCULO \_ DEL SISTEMA DE \_ ROLES</span><span class="sxs-lookup"><span data-stu-id="386e2-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="386e2-422">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ LINK**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="386e2-423">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-424">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="386e2-425">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-425">accHitTest</span></span>
-   <span data-ttu-id="386e2-426">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-426">accLocation</span></span>
-   <span data-ttu-id="386e2-427">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-427">accNavigate</span></span>
-   <span data-ttu-id="386e2-428">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-428">get\_accChild</span></span>
-   <span data-ttu-id="386e2-429">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-429">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-430">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="386e2-431">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="386e2-431">get\_accDescription</span></span>
-   <span data-ttu-id="386e2-432">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-432">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-433">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-434">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-434">get\_accName</span></span>
-   <span data-ttu-id="386e2-435">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-435">get\_accParent</span></span>
-   <span data-ttu-id="386e2-436">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-436">get\_accRole</span></span>
-   <span data-ttu-id="386e2-437">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-437">get\_accState</span></span>
-   <span data-ttu-id="386e2-438">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="386e2-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="386e2-439">PANEL \_ SISTEMA DE \_ ROL</span><span class="sxs-lookup"><span data-stu-id="386e2-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="386e2-440">Para obtener más información sobre este rol, vea [**PANEL DEL SISTEMA DE \_ \_ ROLES**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="386e2-441">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-442">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-442">accHitTest</span></span>
-   <span data-ttu-id="386e2-443">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-443">accLocation</span></span>
-   <span data-ttu-id="386e2-444">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-444">accNavigate</span></span>
-   <span data-ttu-id="386e2-445">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-445">get\_accChild</span></span>
-   <span data-ttu-id="386e2-446">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-446">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-447">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-447">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-448">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-448">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-449">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-450">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-451">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-451">get\_accName</span></span>
-   <span data-ttu-id="386e2-452">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-452">get\_accParent</span></span>
-   <span data-ttu-id="386e2-453">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-453">get\_accRole</span></span>
-   <span data-ttu-id="386e2-454">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="386e2-455">FILA \_ DEL SISTEMA DE \_ ROL</span><span class="sxs-lookup"><span data-stu-id="386e2-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="386e2-456">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ ROW**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="386e2-457">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-458">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-458">accHitTest</span></span>
-   <span data-ttu-id="386e2-459">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-459">accLocation</span></span>
-   <span data-ttu-id="386e2-460">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-460">accNavigate</span></span>
-   <span data-ttu-id="386e2-461">accSelect</span><span class="sxs-lookup"><span data-stu-id="386e2-461">accSelect</span></span>
-   <span data-ttu-id="386e2-462">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-462">get\_accChild</span></span>
-   <span data-ttu-id="386e2-463">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-463">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-464">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="386e2-464">get\_accDescription</span></span>
-   <span data-ttu-id="386e2-465">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-465">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-466">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-466">get\_accName</span></span>
-   <span data-ttu-id="386e2-467">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-467">get\_accParent</span></span>
-   <span data-ttu-id="386e2-468">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-468">get\_accRole</span></span>
-   <span data-ttu-id="386e2-469">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-469">get\_accState</span></span>
-   <span data-ttu-id="386e2-470">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="386e2-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="386e2-471">ROLE \_ SYSTEM \_ ROWHEADER</span><span class="sxs-lookup"><span data-stu-id="386e2-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="386e2-472">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ ROWHEADER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="386e2-473">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-474">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-474">accHitTest</span></span>
-   <span data-ttu-id="386e2-475">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-475">accLocation</span></span>
-   <span data-ttu-id="386e2-476">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-476">accNavigate</span></span>
-   <span data-ttu-id="386e2-477">accSelect</span><span class="sxs-lookup"><span data-stu-id="386e2-477">accSelect</span></span>
-   <span data-ttu-id="386e2-478">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-478">get\_accChild</span></span>
-   <span data-ttu-id="386e2-479">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-479">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-480">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="386e2-481">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="386e2-481">get\_accDescription</span></span>
-   <span data-ttu-id="386e2-482">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-482">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-483">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-483">get\_accName</span></span>
-   <span data-ttu-id="386e2-484">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-484">get\_accParent</span></span>
-   <span data-ttu-id="386e2-485">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-485">get\_accRole</span></span>
-   <span data-ttu-id="386e2-486">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-486">get\_accState</span></span>
-   <span data-ttu-id="386e2-487">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="386e2-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="386e2-488">SEPARADOR \_ DEL SISTEMA DE \_ ROLES</span><span class="sxs-lookup"><span data-stu-id="386e2-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="386e2-489">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ SEPARATOR**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="386e2-490">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-491">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-491">accHitTest</span></span>
-   <span data-ttu-id="386e2-492">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-492">accLocation</span></span>
-   <span data-ttu-id="386e2-493">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-493">get\_accChild</span></span>
-   <span data-ttu-id="386e2-494">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-494">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-495">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-495">get\_accParent</span></span>
-   <span data-ttu-id="386e2-496">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-496">get\_accRole</span></span>
-   <span data-ttu-id="386e2-497">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="386e2-498">SONIDO \_ DEL SISTEMA DE \_ ROL</span><span class="sxs-lookup"><span data-stu-id="386e2-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="386e2-499">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ SOUND**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="386e2-500">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-501">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="386e2-501">get\_accDescription</span></span>
-   <span data-ttu-id="386e2-502">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-502">get\_accName</span></span>
-   <span data-ttu-id="386e2-503">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-503">get\_accRole</span></span>
-   <span data-ttu-id="386e2-504">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="386e2-505">ROLE \_ SYSTEM \_ SPLITBUTTON</span><span class="sxs-lookup"><span data-stu-id="386e2-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="386e2-506">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ SPLITBUTTON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="386e2-507">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="386e2-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-509">accHitTest</span></span>
-   <span data-ttu-id="386e2-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-510">accLocation</span></span>
-   <span data-ttu-id="386e2-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-511">accNavigate</span></span>
-   <span data-ttu-id="386e2-512">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="386e2-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="386e2-513">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-513">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-514">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-515">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-516">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-516">get\_accName</span></span>
-   <span data-ttu-id="386e2-517">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-517">get\_accParent</span></span>
-   <span data-ttu-id="386e2-518">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-518">get\_accRole</span></span>
-   <span data-ttu-id="386e2-519">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="386e2-520">TABLA \_ DEL SISTEMA DE \_ ROLES</span><span class="sxs-lookup"><span data-stu-id="386e2-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="386e2-521">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ TABLE**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="386e2-522">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="386e2-523">accHitTest</span></span>
-   <span data-ttu-id="386e2-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-524">accLocation</span></span>
-   <span data-ttu-id="386e2-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="386e2-525">accNavigate</span></span>
-   <span data-ttu-id="386e2-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="386e2-526">accSelect</span></span>
-   <span data-ttu-id="386e2-527">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="386e2-527">get\_accChild</span></span>
-   <span data-ttu-id="386e2-528">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="386e2-528">get\_accChildCount</span></span>
-   <span data-ttu-id="386e2-529">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="386e2-529">get\_accDescription</span></span>
-   <span data-ttu-id="386e2-530">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="386e2-530">get\_accFocus</span></span>
-   <span data-ttu-id="386e2-531">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="386e2-531">get\_accHelp</span></span>
-   <span data-ttu-id="386e2-532">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="386e2-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="386e2-533">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="386e2-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="386e2-534">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="386e2-534">get\_accName</span></span>
-   <span data-ttu-id="386e2-535">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-535">get\_accParent</span></span>
-   <span data-ttu-id="386e2-536">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-536">get\_accRole</span></span>
-   <span data-ttu-id="386e2-537">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="386e2-538">ESPACIO \_ EN BLANCO DEL SISTEMA DE \_ ROLES</span><span class="sxs-lookup"><span data-stu-id="386e2-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="386e2-539">Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ WHITESPACE**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="386e2-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="386e2-540">**Propiedades y métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="386e2-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="386e2-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="386e2-541">accLocation</span></span>
-   <span data-ttu-id="386e2-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="386e2-542">accSelect</span></span>
-   <span data-ttu-id="386e2-543">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="386e2-543">get\_accParent</span></span>
-   <span data-ttu-id="386e2-544">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="386e2-544">get\_accRole</span></span>
-   <span data-ttu-id="386e2-545">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="386e2-545">get\_accState</span></span>

 

 