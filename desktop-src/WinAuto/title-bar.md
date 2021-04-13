---
title: Barra de título (referencia de elementos de interfaz de usuario de MSAA)
description: En la barra de título de la parte superior de una ventana se muestra un icono y una línea de texto definidos por la aplicación.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fee3642a67be85b27eac6a73ac7c452f2349d1
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420181"
---
# <a name="title-bar-msaa-ui-element-reference"></a><span data-ttu-id="04621-103">Barra de título (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="04621-103">Title Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="04621-104">En este tema se describen los objetos de **barra de título** para la referencia de elementos de interfaz de usuario de MSAA.</span><span class="sxs-lookup"><span data-stu-id="04621-104">This topic describes **Title Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="04621-105">La forma de crear objetos de **barra de título** en varios marcos de interfaz de usuario no se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="04621-105">How to create **Title Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="04621-106">Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.</span><span class="sxs-lookup"><span data-stu-id="04621-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="04621-107">En la barra de título de la parte superior de una ventana se muestra un icono y una línea de texto definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04621-107">The title bar at the top of a window displays an application-defined icon and line of text.</span></span> <span data-ttu-id="04621-108">El texto especifica el nombre de la aplicación e indica el propósito de la ventana.</span><span class="sxs-lookup"><span data-stu-id="04621-108">The text specifies the name of the application and indicates the purpose of the window.</span></span> <span data-ttu-id="04621-109">La barra de título también permite que el usuario mueva la ventana con un mouse u otro dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="04621-109">The title bar also makes it possible for the user to move the window using a mouse or other pointing device.</span></span>

<span data-ttu-id="04621-110">Las barras de título contienen al menos tres botones pequeños que minimizan, maximizan o restauran, y cierran la ventana asociada a la barra de título.</span><span class="sxs-lookup"><span data-stu-id="04621-110">Title bars contain at least three small buttons that minimize, maximize or restore, and close the window associated with the title bar.</span></span> <span data-ttu-id="04621-111">Las barras de título también contienen un botón ayuda contextual.</span><span class="sxs-lookup"><span data-stu-id="04621-111">Title bars also contain a context-sensitive Help button.</span></span> <span data-ttu-id="04621-112">Las aplicaciones que se ejecutan en la versión Far-East del sistema operativo Windows también pueden contener botones del editor de métodos de entrada (IME).</span><span class="sxs-lookup"><span data-stu-id="04621-112">Applications running in the Far-East version of the Windows operating system may also contain Input Method Editor (IME) buttons.</span></span> <span data-ttu-id="04621-113">Microsoft Active Accessibility expone estos botones como elementos secundarios de la barra de título.</span><span class="sxs-lookup"><span data-stu-id="04621-113">Microsoft Active Accessibility exposes these buttons as child elements of the title bar.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="04621-114">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="04621-114">IAccessible Methods</span></span>

<span data-ttu-id="04621-115">Las barras de título admiten los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="04621-115">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="04621-116">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="04621-116">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="04621-117">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="04621-117">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="04621-118">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="04621-118">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="04621-119">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="04621-119">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="04621-120">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="04621-120">IAccessible Properties</span></span>

<span data-ttu-id="04621-121">Las barras de título admiten las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="04621-121">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04621-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04621-122">Property</span></span></th>
<th><span data-ttu-id="04621-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04621-123">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04621-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="04621-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="04621-125">La propiedad <strong>ChildCount</strong> es cinco.</span><span class="sxs-lookup"><span data-stu-id="04621-125">The <strong>ChildCount</strong> property is five.</span></span> <span data-ttu-id="04621-126">La propiedad <strong>ChildCount</strong> incluye los botones IME y ayuda contextual incluso cuando no se muestran.</span><span class="sxs-lookup"><span data-stu-id="04621-126">The <strong>ChildCount</strong> property includes the IME and context-sensitive Help buttons even when they are not displayed.</span></span> <span data-ttu-id="04621-127">Los botones que no se muestran tienen la propiedad <strong>State</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="04621-127">Buttons that are not displayed have the <strong>State</strong> property <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04621-128"><strong>get_accDescription</strong></span><span class="sxs-lookup"><span data-stu-id="04621-128"><strong>get_accDescription</strong></span></span></td>
<td><span data-ttu-id="04621-129">La propiedad <strong>Description</strong> de la propia barra de título es: &quot; muestra el nombre de la ventana y contiene controles para manipularla. &quot; Los botones secundarios de la barra de título tienen las siguientes descripciones:</span><span class="sxs-lookup"><span data-stu-id="04621-129">The <strong>Description</strong> property of the title bar itself is: &quot;Displays the name of the window and contains controls to manipulate it.&quot; The child buttons in the title bar have the following descriptions:</span></span><br/>
<ul>
<li><span data-ttu-id="04621-130">&quot;Saca la ventana del</span><span class="sxs-lookup"><span data-stu-id="04621-130">&quot;Moves the window out of</span></span></li>
<li><span data-ttu-id="04621-131">&quot;Hace que la ventana esté completa</span><span class="sxs-lookup"><span data-stu-id="04621-131">&quot;Makes the window full</span></span></li>
<li><span data-ttu-id="04621-132">&quot;Coloca un minimizado o</span><span class="sxs-lookup"><span data-stu-id="04621-132">&quot;Puts a minimized or</span></span></li>
<li><span data-ttu-id="04621-133">&quot;Cierra la ventana&quot;</span><span class="sxs-lookup"><span data-stu-id="04621-133">&quot;Closes the window&quot;</span></span></li>
<li><span data-ttu-id="04621-134">&quot;Entra o sale del contexto-</span><span class="sxs-lookup"><span data-stu-id="04621-134">&quot;Enters or leaves context-</span></span></li>
<li><span data-ttu-id="04621-135">&quot;Muestra el teclado cuando se presiona&quot;</span><span class="sxs-lookup"><span data-stu-id="04621-135">&quot;Brings up the keyboard when pressed&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04621-136"><strong>get_accName</strong></span><span class="sxs-lookup"><span data-stu-id="04621-136"><strong>get_accName</strong></span></span></td>
<td><span data-ttu-id="04621-137">La barra de título no admite la propiedad <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="04621-137">The title bar itself does not support the <strong>Name</strong> property.</span></span> <span data-ttu-id="04621-138">Los botones secundarios de la barra de título tienen los nombres siguientes:</span><span class="sxs-lookup"><span data-stu-id="04621-138">The child buttons in the title bar have the following names:</span></span>
<ul>
<li><span data-ttu-id="04621-139">&quot;Minimizar&quot;</span><span class="sxs-lookup"><span data-stu-id="04621-139">&quot;Minimize&quot;</span></span></li>
<li><span data-ttu-id="04621-140">&quot;Maximizar &quot; o &quot; restaurar &quot; ,</span><span class="sxs-lookup"><span data-stu-id="04621-140">&quot;Maximize&quot; or &quot;Restore&quot;,</span></span></li>
<li><span data-ttu-id="04621-141">&quot;Close&quot;</span><span class="sxs-lookup"><span data-stu-id="04621-141">&quot;Close&quot;</span></span></li>
<li><span data-ttu-id="04621-142">&quot;Ayuda contextual&quot;</span><span class="sxs-lookup"><span data-stu-id="04621-142">&quot;Context help&quot;</span></span></li>
<li><span data-ttu-id="04621-143">&quot;IME&quot;</span><span class="sxs-lookup"><span data-stu-id="04621-143">&quot;IME&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04621-144"><strong>get_accParent</strong></span><span class="sxs-lookup"><span data-stu-id="04621-144"><strong>get_accParent</strong></span></span></td>
<td><span data-ttu-id="04621-145">La propiedad <strong>primaria</strong> de la barra de título es la ventana principal de la aplicación ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) que tiene el mismo nombre de clase de ventana definida por la aplicación que la barra de título.</span><span class="sxs-lookup"><span data-stu-id="04621-145">The <strong>Parent</strong> property of the title bar is the main application window ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) that has the same application-defined window class name as the title bar.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04621-146"><strong>get_accRole</strong></span><span class="sxs-lookup"><span data-stu-id="04621-146"><strong>get_accRole</strong></span></span></td>
<td><span data-ttu-id="04621-147">La propiedad de <strong>rol</strong> es <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="04621-147">The <strong>Role</strong> property is <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>.</span></span> <span data-ttu-id="04621-148">Los botones secundarios de la barra de título tienen la propiedad de <strong>rol</strong> <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="04621-148">The child buttons in the title bar have the <strong>Role</strong> property <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04621-149"><strong>get_accState</strong></span><span class="sxs-lookup"><span data-stu-id="04621-149"><strong>get_accState</strong></span></span></td>
<td><span data-ttu-id="04621-150">La propiedad <strong>Estado</strong> de la barra de título y los botones secundarios puede ser una combinación de uno o varios de los <a href="object-state-constants.md">valores</a>siguientes: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="04621-150">The <strong>State</strong> property for the title bar and the child buttons can be a combination of one or more of the following <a href="object-state-constants.md">values</a>: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04621-151"><strong>get_accValue</strong></span><span class="sxs-lookup"><span data-stu-id="04621-151"><strong>get_accValue</strong></span></span></td>
<td><span data-ttu-id="04621-152">La propiedad <strong>Value</strong> es una cadena que es igual que el texto que se muestra en la barra de título.</span><span class="sxs-lookup"><span data-stu-id="04621-152">The <strong>Value</strong> property is a string that is the same as the text displayed in the title bar.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="04621-153">Notas</span><span class="sxs-lookup"><span data-stu-id="04621-153">Notes</span></span>

-   <span data-ttu-id="04621-154">Aunque la barra de título de una aplicación tiene el indicador de estado de la marca de la propiedad **State** , nunca tiene el sistema de estado de marca **de estado** [**\_ \_ centrado**](object-state-constants.md). [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="04621-154">Although an application's title bar has the **State** property flag [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md), it never has the **State** flag [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md).</span></span> <span data-ttu-id="04621-155">Establecer el foco en un objeto de barra de título se centra en la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04621-155">Setting focus to a title bar object focuses the application window.</span></span>
-   <span data-ttu-id="04621-156">Dado que el objeto de barra de título no admite [**Get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), los botones de la barra de título son elementos simples.</span><span class="sxs-lookup"><span data-stu-id="04621-156">Because the title bar object does not support [**get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), the buttons on the title bar are simple elements.</span></span> <span data-ttu-id="04621-157">No admiten la propia interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="04621-157">They do not support the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface themselves.</span></span> <span data-ttu-id="04621-158">El objeto de barra de título proporciona información sobre estos botones secundarios.</span><span class="sxs-lookup"><span data-stu-id="04621-158">The title bar object provides information about these child buttons.</span></span>
-   <span data-ttu-id="04621-159">Dado que las barras de título no obtienen el foco y no tienen ninguna acción predeterminada, los métodos [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) y [**Get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) no se admiten para este control.</span><span class="sxs-lookup"><span data-stu-id="04621-159">Because title bars do not get focus and have no default action, the [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) and [**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) methods are not supported for this control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04621-160">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04621-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04621-161">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="04621-161">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





