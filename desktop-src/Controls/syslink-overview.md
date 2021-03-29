---
title: Acerca de los controles SysLink
description: Un control SysLink es una ventana que representa texto marcado y notifica a la aplicación cuando los usuarios hacen clic en sus hipervínculos incrustados. Este control proporciona una alternativa práctica al uso del botón de vínculo de comando. Para obtener más información, vea tipos de botón.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb0d15cac479b844b0ea8510c34cc57f56822be
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078433"
---
# <a name="about-syslink-controls"></a><span data-ttu-id="38028-105">Acerca de los controles SysLink</span><span class="sxs-lookup"><span data-stu-id="38028-105">About SysLink Controls</span></span>

<span data-ttu-id="38028-106">Un control SysLink es una ventana que representa texto marcado y notifica a la aplicación cuando los usuarios hacen clic en sus hipervínculos incrustados.</span><span class="sxs-lookup"><span data-stu-id="38028-106">A SysLink control is a window that renders marked-up text, and notifies the application when users click its embedded hyperlinks.</span></span> <span data-ttu-id="38028-107">Este control proporciona una alternativa práctica al uso del [**botón de vínculo de comando**](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="38028-107">This control provides a convenient alternative to using the [**Command link button**](button-styles.md).</span></span> <span data-ttu-id="38028-108">Para obtener más información, vea [tipos de botón](button-types-and-styles.md).</span><span class="sxs-lookup"><span data-stu-id="38028-108">For more information, see [Button Types](button-types-and-styles.md).</span></span>

<span data-ttu-id="38028-109">Cada control SysLink puede admitir varios hipervínculos, y puede tener acceso a cada hipervínculo a través de un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="38028-109">Each SysLink control can support multiple hyperlinks, and you can access each hyperlink through a zero-based index.</span></span> <span data-ttu-id="38028-110">El control SysLink se define en el ComCtl32.dll versión 6 y requiere un manifiesto o una directiva que especifique que se debe usar la versión 6 del archivo DLL si está disponible.</span><span class="sxs-lookup"><span data-stu-id="38028-110">The SysLink control is defined in the ComCtl32.dll version 6, and it requires a manifest or directive that specifies that version 6 of the DLL should be used if it is available.</span></span> <span data-ttu-id="38028-111">Para obtener más información, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="38028-111">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

<span data-ttu-id="38028-112">Este artículo contiene las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="38028-112">This article contains the following sections.</span></span>

-   [<span data-ttu-id="38028-113">Marcado de SysLink</span><span class="sxs-lookup"><span data-stu-id="38028-113">SysLink Markup</span></span>](#syslink-markup)
-   [<span data-ttu-id="38028-114">Atributos de vínculo</span><span class="sxs-lookup"><span data-stu-id="38028-114">Link Attributes</span></span>](#link-attributes)
-   [<span data-ttu-id="38028-115">Estados de vínculo</span><span class="sxs-lookup"><span data-stu-id="38028-115">Link States</span></span>](#link-states)
-   [<span data-ttu-id="38028-116">Limitaciones de la presentación de texto bidireccional</span><span class="sxs-lookup"><span data-stu-id="38028-116">Limitations on Bidirectional Text Display</span></span>](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a><span data-ttu-id="38028-117">Marcado de SysLink</span><span class="sxs-lookup"><span data-stu-id="38028-117">SysLink Markup</span></span>

<span data-ttu-id="38028-118">El control SysLink admite la etiqueta delimitadora ( &lt; a &gt; ) junto con los atributos **href** e **ID**.</span><span class="sxs-lookup"><span data-stu-id="38028-118">The SysLink control supports the anchor tag(&lt;a&gt;) along with the attributes **HREF** and **ID**.</span></span> <span data-ttu-id="38028-119">Un **href** puede ser cualquier protocolo, como http, FTP y mailto.</span><span class="sxs-lookup"><span data-stu-id="38028-119">An **HREF** can be any protocol, such as http, ftp, and mailto.</span></span> <span data-ttu-id="38028-120">Un **identificador** es un nombre opcional, único dentro de un control SysLink, y está asociado a un vínculo individual.</span><span class="sxs-lookup"><span data-stu-id="38028-120">An **ID** is an optional name, unique within a SysLink control, and it is associated with an individual link.</span></span> <span data-ttu-id="38028-121">A los vínculos también se les asigna un índice basado en cero según su posición dentro de la cadena.</span><span class="sxs-lookup"><span data-stu-id="38028-121">Links are also assigned a zero-based index according to their position within the string.</span></span> <span data-ttu-id="38028-122">Este índice se utiliza para tener acceso a un vínculo.</span><span class="sxs-lookup"><span data-stu-id="38028-122">This index is used to access a link.</span></span>

## <a name="link-attributes"></a><span data-ttu-id="38028-123">Atributos de vínculo</span><span class="sxs-lookup"><span data-stu-id="38028-123">Link Attributes</span></span>

<span data-ttu-id="38028-124">Los atributos de cada vínculo se pueden establecer en la etiqueta delimitadora para cada vínculo o mediante el envío del mensaje [**LM \_ SETITEM**](lm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="38028-124">Each link's attributes can be set either within the anchor tag for each link or by sending the [**LM\_SETITEM**](lm-setitem.md) message.</span></span> <span data-ttu-id="38028-125">La configuración de un atributo mediante su especificación en la cadena de inicialización simplemente inicializa el valor.</span><span class="sxs-lookup"><span data-stu-id="38028-125">Setting an attribute by specifying it within the initialization string merely initializes the value.</span></span> <span data-ttu-id="38028-126">Puede cambiar el valor de un atributo mediante el uso posterior del mensaje **de \_ SETITEM de LM** .</span><span class="sxs-lookup"><span data-stu-id="38028-126">You can change the value of an attribute through subsequent use of the **LM\_SETITEM** message.</span></span>

## <a name="link-states"></a><span data-ttu-id="38028-127">Estados de vínculo</span><span class="sxs-lookup"><span data-stu-id="38028-127">Link States</span></span>

<span data-ttu-id="38028-128">Los elementos de vínculo pueden estar en cualquiera de los tres Estados, representados por las marcas de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="38028-128">Link items can be in any one of three states, represented by the flags in the following table.</span></span>



| <span data-ttu-id="38028-129">Marca de estado</span><span class="sxs-lookup"><span data-stu-id="38028-129">State flag</span></span>   | <span data-ttu-id="38028-130">Apariencia y significado</span><span class="sxs-lookup"><span data-stu-id="38028-130">Appearance and meaning</span></span>                                            |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="38028-131">LIS \_ centrado</span><span class="sxs-lookup"><span data-stu-id="38028-131">LIS\_FOCUSED</span></span> | <span data-ttu-id="38028-132">El vínculo tiene el foco de teclado y al presionar entrar se activa.</span><span class="sxs-lookup"><span data-stu-id="38028-132">The link has the keyboard focus, and pressing Enter activates it.</span></span> |
| <span data-ttu-id="38028-133">LIS \_ habilitado</span><span class="sxs-lookup"><span data-stu-id="38028-133">LIS\_ENABLED</span></span> | <span data-ttu-id="38028-134">El vínculo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="38028-134">The link is enabled.</span></span>                                              |
| <span data-ttu-id="38028-135">LIS \_ visitado</span><span class="sxs-lookup"><span data-stu-id="38028-135">LIS\_VISITED</span></span> | <span data-ttu-id="38028-136">El usuario ya ha visitado la dirección URL representada por el vínculo.</span><span class="sxs-lookup"><span data-stu-id="38028-136">The user has already visited the URL represented by the link.</span></span>     |



 

## <a name="limitations-on-bidirectional-text-display"></a><span data-ttu-id="38028-137">Limitaciones de la presentación de texto bidireccional</span><span class="sxs-lookup"><span data-stu-id="38028-137">Limitations on Bidirectional Text Display</span></span>

<span data-ttu-id="38028-138">Algunos idiomas, como el árabe o el hebreo, se escriben de derecha a izquierda (RTL); El inglés se escribe de izquierda a derecha (LTR).</span><span class="sxs-lookup"><span data-stu-id="38028-138">Some languages, such as Arabic or Hebrew, are written right-to-left (RTL); English is written left-to-right (LTR).</span></span> <span data-ttu-id="38028-139">La combinación de RTL con LTR se denomina texto bidireccional.</span><span class="sxs-lookup"><span data-stu-id="38028-139">Combining RTL with LTR is called bidirectional text.</span></span> <span data-ttu-id="38028-140">No se puede producir el resultado esperado cuando se usa un control SysLink para mezclar construcciones de marcado direccionales Unicode o con Unicode de LTR y RTL en cadenas de recursos, como marcadores de flujo bidireccionales para controlar el flujo de cadenas.</span><span class="sxs-lookup"><span data-stu-id="38028-140">Mixing LTR and RTL Unicode or HTML directional markup constructs in resource strings, as bidirectional flow markers to control the flow of strings, may not produce the expected result when using a SysLink control.</span></span> <span data-ttu-id="38028-141">Por ejemplo, es posible que una oración marcada por LTR no se muestre correctamente en el contexto RTL.</span><span class="sxs-lookup"><span data-stu-id="38028-141">For instance, an LTR-marked sentence may not display correctly in RTL context.</span></span>

> [!Note]  
> <span data-ttu-id="38028-142">Los controles SysLink no admiten la presentación bidireccional en todos los escenarios.</span><span class="sxs-lookup"><span data-stu-id="38028-142">SysLink controls do not support bidirectional display under all scenarios.</span></span> <span data-ttu-id="38028-143">Use un control SysLink solo si sabe que un diseño de LTR o RTL sencillo es adecuado.</span><span class="sxs-lookup"><span data-stu-id="38028-143">Use a SysLink control only if you know that a simple LTR or RTL layout is adequate.</span></span> <span data-ttu-id="38028-144">En caso contrario, considere la posibilidad de usar una tecnología más avanzada, como [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="38028-144">Otherwise, consider using a more advanced technology such as [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).</span></span>

 

 

 