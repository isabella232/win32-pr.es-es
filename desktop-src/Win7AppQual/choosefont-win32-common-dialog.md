---
description: .
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: Cuadro de diálogo común de Win32 ChooseFont ()
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e55a31d1f4d5530e04fe455135952eb94cc4bda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717132"
---
# <a name="choosefont-win32-common-dialog"></a><span data-ttu-id="8612c-103">Cuadro de diálogo común de Win32 ChooseFont ()</span><span class="sxs-lookup"><span data-stu-id="8612c-103">ChooseFont() Win32 Common Dialog</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="8612c-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="8612c-104">Affected Platforms</span></span>

<span data-ttu-id="8612c-105">**Clientes** : Windows 7</span><span class="sxs-lookup"><span data-stu-id="8612c-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="8612c-106">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8612c-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="8612c-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="8612c-107">Feature Impact</span></span>

<span data-ttu-id="8612c-108">**Gravedad** baja</span><span class="sxs-lookup"><span data-stu-id="8612c-108">**Severity** - Low</span></span>  
<span data-ttu-id="8612c-109">**Frecuencia** : medio</span><span class="sxs-lookup"><span data-stu-id="8612c-109">**Frequency** - Medium</span></span>  




## <a name="description"></a><span data-ttu-id="8612c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8612c-110">Description</span></span>

<span data-ttu-id="8612c-111">Windows 7 incluye varias actualizaciones en el cuadro de diálogo común de Win32 ChooseFont ().</span><span class="sxs-lookup"><span data-stu-id="8612c-111">Windows 7 includes several updates to the ChooseFont() Win32 common dialog.</span></span> <span data-ttu-id="8612c-112">Estas se dividen en dos categorías:</span><span class="sxs-lookup"><span data-stu-id="8612c-112">These fall into two categories:</span></span>

-   <span data-ttu-id="8612c-113">Actualización visual del cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="8612c-113">Visual refresh of the dialog</span></span>
-   <span data-ttu-id="8612c-114">Compatibilidad con las nuevas características de mostrar u ocultar fuentes</span><span class="sxs-lookup"><span data-stu-id="8612c-114">Support for new show/hide fonts feature</span></span>

<span data-ttu-id="8612c-115">La **actualización del cuadro de diálogo** actualiza la plantilla estándar para que el cuadro de diálogo se muestre más en línea con otros diseños de cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="8612c-115">The **dialog refresh** updates the standard template to bring the dialog more in line with other dialog layouts in Windows.</span></span> <span data-ttu-id="8612c-116">Presenta WYSIWYG a las listas de presentación de fuentes para ayudar a los usuarios a elegir fuentes.</span><span class="sxs-lookup"><span data-stu-id="8612c-116">It introduces WYSIWYG to the font display lists to help users choose fonts.</span></span> <span data-ttu-id="8612c-117">También incluye un vínculo al CPL Fonts para facilitar el acceso a los usuarios que deseen personalizar sus listas de fuentes.</span><span class="sxs-lookup"><span data-stu-id="8612c-117">It also includes a link to the Fonts CPL to provide easy access for users wishing to customize their font lists.</span></span>

<span data-ttu-id="8612c-118">**Mostrar u ocultar fuentes** es una nueva característica de la plataforma Windows 7 en la que las fuentes no adecuadas para la configuración de idioma del usuario actual (métodos de entrada) no se presentan de forma predeterminada en las listas de selección de fuentes.</span><span class="sxs-lookup"><span data-stu-id="8612c-118">**Show/hide fonts** is a new Windows 7 platform feature whereby fonts not appropriate for the current user's language settings (input methods) are not presented by default in font selection lists.</span></span> <span data-ttu-id="8612c-119">Los usuarios pueden personalizar las fuentes que deseen que aparezcan en el CPL de fuentes o deshabilitar esta característica.</span><span class="sxs-lookup"><span data-stu-id="8612c-119">Users may customize the fonts that they wish to appear in the Fonts CPL or may disable this feature.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="8612c-120">Manifiesto de impacto</span><span class="sxs-lookup"><span data-stu-id="8612c-120">Manifestation of Impact</span></span>

<span data-ttu-id="8612c-121">**Actualización visual del cuadro de diálogo**</span><span class="sxs-lookup"><span data-stu-id="8612c-121">**Dialog visual refresh**</span></span>

<span data-ttu-id="8612c-122">Hemos incorporado dos nuevas plantillas en Windows 7 (una para las aplicaciones que cargan la versión 6 o posterior de comctl32.dll y otra para las aplicaciones que cargan versiones anteriores).</span><span class="sxs-lookup"><span data-stu-id="8612c-122">We have introduced two new templates in Windows 7 (one for applications that load version 6 or later of comctl32.dll and another for applications loading earlier versions).</span></span>

-   <span data-ttu-id="8612c-123">Por motivos de compatibilidad de aplicaciones, estas nuevas plantillas solo se cargan para las aplicaciones que no enlazan la cola de mensajes ChooseFont.</span><span class="sxs-lookup"><span data-stu-id="8612c-123">For application compatibility reasons, these new templates will only be loaded for applications that do not hook the ChooseFont message queue.</span></span> <span data-ttu-id="8612c-124">Las aplicaciones que enlazan la cola de mensajes seguirán viendo el diseño del cuadro de diálogo antiguo.</span><span class="sxs-lookup"><span data-stu-id="8612c-124">Applications that hook the message queue will continue to see the old dialog layout.</span></span>
-   <span data-ttu-id="8612c-125">Las aplicaciones que proporcionan sus propias plantillas seguirán pudiendo usarlas.</span><span class="sxs-lookup"><span data-stu-id="8612c-125">Applications that provide their own templates will continue to be able to use them.</span></span>

<span data-ttu-id="8612c-126">Las aplicaciones que no obtienen las nuevas plantillas no verán cambios de diseño de cuadros de diálogo de vista.</span><span class="sxs-lookup"><span data-stu-id="8612c-126">Applications that do not get the new templates will see no dialog layout changes from Vista.</span></span> <span data-ttu-id="8612c-127">Sin embargo, todavía deben obtener la nueva versión preliminar de la fuente WYSIWYG.</span><span class="sxs-lookup"><span data-stu-id="8612c-127">They should however still get the new WYSIWYG font preview.</span></span>

<span data-ttu-id="8612c-128">**Mostrar u ocultar fuentes**</span><span class="sxs-lookup"><span data-stu-id="8612c-128">**Show/hide fonts**</span></span>

<span data-ttu-id="8612c-129">En todas las versiones de ChooseFont, el cuadro de diálogo usará la configuración de fuente Mostrar u ocultar del usuario actual para determinar la lista de fuentes que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="8612c-129">For all versions of ChooseFont, the dialog will use the current user's show/hide font settings to determine the font list to display.</span></span> <span data-ttu-id="8612c-130">Esto hará que se muestren menos listas de fuentes en la mayoría de las instancias.</span><span class="sxs-lookup"><span data-stu-id="8612c-130">This will result in the display of fewer font lists in most instances.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="8612c-131">Mitigación del usuario final</span><span class="sxs-lookup"><span data-stu-id="8612c-131">End-user Mitigation</span></span>

<span data-ttu-id="8612c-132">**Mostrar u ocultar fuentes:** Para deshabilitar la ocultación de fuentes, los usuarios deben ir a la página de configuración de fuentes del CPL de fuentes y anular la selección del</span><span class="sxs-lookup"><span data-stu-id="8612c-132">**Show/Hide Fonts:** To disable font hiding, users should go to the Font Settings page in the Fonts CPL and deselect the '</span></span>

<span data-ttu-id="8612c-133">Casilla "ocultar fuentes según la configuración de idioma"</span><span class="sxs-lookup"><span data-stu-id="8612c-133">"Hide fonts based on language settings" checkbox</span></span>

## <a name="developer-mitigation"></a><span data-ttu-id="8612c-134">Mitigación del desarrollador</span><span class="sxs-lookup"><span data-stu-id="8612c-134">Developer Mitigation</span></span>

-   <span data-ttu-id="8612c-135">**Actualización visual:** Los desarrolladores de aplicaciones que proporcionan sus propias plantillas pueden querer actualizar esto para que esté en línea con la nueva plantilla de Windows 7 adecuada.</span><span class="sxs-lookup"><span data-stu-id="8612c-135">**Visual refresh:** Applications developers who provide their own templates may want to refresh this to be in line with the appropriate new Windows 7 template.</span></span> <span data-ttu-id="8612c-136">Las nuevas plantillas están disponibles en el archivo de plantilla Font. Dlg.</span><span class="sxs-lookup"><span data-stu-id="8612c-136">The new templates are available in the Font.dlg template file.</span></span>

    <span data-ttu-id="8612c-137">**Nota:** La nueva plantilla publicada contiene un control SysLink adicional que proporciona un acceso directo que permite a los usuarios iniciar el CPL Fonts para mostrar más fuentes.</span><span class="sxs-lookup"><span data-stu-id="8612c-137">**Note:** The new published template contains an additional SysLink control that provides a shortcut that allows users to launch the Fonts CPL to display more fonts.</span></span> <span data-ttu-id="8612c-138">El control de vínculo requiere la versión 6 de la biblioteca de controles comunes de Windows (comctl32.dll).</span><span class="sxs-lookup"><span data-stu-id="8612c-138">The link control requires version 6 of the Windows common control library (comctl32.dll).</span></span> <span data-ttu-id="8612c-139">Los desarrolladores deben proporcionar un manifiesto o una directiva que especifique el uso de la versión 6 del archivo DLL si está disponible.</span><span class="sxs-lookup"><span data-stu-id="8612c-139">Developers should provide a manifest or directive that specifies the use of version 6 of the DLL if available.</span></span> <span data-ttu-id="8612c-140">En el caso de que una aplicación use una versión anterior de la biblioteca de controles comunes, use en su lugar el tipo de control "PUSHBUTTON".</span><span class="sxs-lookup"><span data-stu-id="8612c-140">Where an application uses an earlier version of the common control library, use the "PUSHBUTTON" control type instead.</span></span>

-   <span data-ttu-id="8612c-141">**Mostrar u ocultar fuentes:** Los desarrolladores pueden deshabilitar esta característica proporcionando una marca adicional (CF \_ INACTIVEFONTS) en el miembro flags de la estructura CHOOSEFONT.</span><span class="sxs-lookup"><span data-stu-id="8612c-141">**Show/Hide Fonts:** Developers may disable this feature by providing an additional flag (CF\_INACTIVEFONTS) in the flags member of the CHOOSEFONT structure.</span></span> <span data-ttu-id="8612c-142">Al establecer esta marca, se muestran todas las fuentes instaladas en la lista fuente.</span><span class="sxs-lookup"><span data-stu-id="8612c-142">Setting this flag causes all installed fonts to display in the font list.</span></span>
-   <span data-ttu-id="8612c-143">**Mostrar u ocultar fuentes:** Las aplicaciones que proporcionan contenido de la ayuda de ChooseFont pueden querer agregar contenido para explicar por qué se reduce la lista de fuentes y dirigir a los usuarios al CPL de fuentes para personalizar sus listas de fuentes.</span><span class="sxs-lookup"><span data-stu-id="8612c-143">**Show/Hide Fonts:** Applications that provide ChooseFont help content may wish to add content to explain why the font list is reduced and direct users to the Fonts CPL to customize their font lists.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="8612c-144">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="8612c-144">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="8612c-145">Los desarrolladores cuyas aplicaciones enlazan la cola de mensajes ChooseFont para personalizar el cuadro de diálogo deben comprobar que sus aplicaciones conservan toda la funcionalidad existente.</span><span class="sxs-lookup"><span data-stu-id="8612c-145">Developers whose applications hook the ChooseFont message queue to customize the dialog should verify that their applications retain all existing functionality.</span></span>

<span data-ttu-id="8612c-146">Las aplicaciones que recortan drásticamente la lista de fuentes mediante marcas deben asegurarse de que la lista de fuentes presentada siga siendo aceptable.</span><span class="sxs-lookup"><span data-stu-id="8612c-146">Applications that heavily trim the font list using flags should ensure that the font list presented remains acceptable.</span></span>

 

 



