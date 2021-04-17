---
description: Evolución de la compatibilidad de MUI entre versiones de Windows
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Evolución de la compatibilidad de MUI entre versiones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b896c3651cbea3eef8f2d2021194742f24818f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687772"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a><span data-ttu-id="86ca3-103">Evolución de la compatibilidad de MUI entre versiones de Windows</span><span class="sxs-lookup"><span data-stu-id="86ca3-103">Evolution of MUI Support across Windows Versions</span></span>

-   [<span data-ttu-id="86ca3-104">Antes de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86ca3-104">Before Windows Vista</span></span>](#before-windows-vista)
-   [<span data-ttu-id="86ca3-105">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="86ca3-105">Windows Vista and Beyond</span></span>](#windows-vista-and-beyond)
    -   [<span data-ttu-id="86ca3-106">Un sistema operativo independiente de idioma o MUI</span><span class="sxs-lookup"><span data-stu-id="86ca3-106">A language neutral/MUI operating system</span></span>](#a-language-neutralmui-operating-system)
    -   [<span data-ttu-id="86ca3-107">Los escenarios de implementación están totalmente basados en MUI</span><span class="sxs-lookup"><span data-stu-id="86ca3-107">Deployment scenarios are fully MUI-based</span></span>](#deployment-scenarios-are-fully-mui-based)
    -   [<span data-ttu-id="86ca3-108">Implementación de una sola imagen</span><span class="sxs-lookup"><span data-stu-id="86ca3-108">Single image deployment</span></span>](#single-image-deployment)
    -   [<span data-ttu-id="86ca3-109">Modelo de servicio mejorado</span><span class="sxs-lookup"><span data-stu-id="86ca3-109">Improved servicing model</span></span>](#improved-servicing-model)
    -   [<span data-ttu-id="86ca3-110">Infraestructura de MUI</span><span class="sxs-lookup"><span data-stu-id="86ca3-110">MUI infrastructure</span></span>](#mui-infrastructure)
    -   [<span data-ttu-id="86ca3-111">Administración de idiomas</span><span class="sxs-lookup"><span data-stu-id="86ca3-111">Language management</span></span>](#language-management)
    -   [<span data-ttu-id="86ca3-112">Administración de recursos</span><span class="sxs-lookup"><span data-stu-id="86ca3-112">Resource handling</span></span>](#resource-handling)

## <a name="before-windows-vista"></a><span data-ttu-id="86ca3-113">Antes de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86ca3-113">Before Windows Vista</span></span>

<span data-ttu-id="86ca3-114">Antes de la versión de Windows Vista, Windows se incluía con imágenes de un solo idioma, lo que significaba que cada versión localizada de Windows contenía un solo idioma para su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="86ca3-114">Prior to the Windows Vista release, Windows shipped with single-language images, which meant that each localized version of Windows contained a single language for its user interface.</span></span> <span data-ttu-id="86ca3-115">MUI era un complemento para la versión en inglés del sistema operativo y los paquetes de interfaz de usuario multilingüe solo se podían agregar a determinadas versiones en Inglés de Windows.</span><span class="sxs-lookup"><span data-stu-id="86ca3-115">MUI was an add-on to the English version of the operating system, and the Multilingual User Interface Packs could only be added to certain English versions of Windows.</span></span> <span data-ttu-id="86ca3-116">Cuando se instala en la versión en Inglés de Windows, MUI permitía cambiar el idioma de la interfaz de usuario del sistema operativo según las preferencias de los usuarios individuales a uno de los idiomas admitidos.</span><span class="sxs-lookup"><span data-stu-id="86ca3-116">When installed on the English version of Windows, MUI allowed the user interface language of the operating system to be changed according to the preferences of individual users to one of the supported languages.</span></span>

<span data-ttu-id="86ca3-117">El modelo de paquete MUI no expondría la compatibilidad de MUI con las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="86ca3-117">The MUI Pack model did not expose MUI support for applications.</span></span> <span data-ttu-id="86ca3-118">Aunque los desarrolladores pueden crear aplicaciones multilingües, tenían que crear sus propios mecanismos para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="86ca3-118">Although developers could create multi-lingual applications, they had to create their own mechanisms to do so.</span></span>

## <a name="windows-vista-and-beyond"></a><span data-ttu-id="86ca3-119">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="86ca3-119">Windows Vista and Beyond</span></span>

<span data-ttu-id="86ca3-120">Con Windows Vista, Microsoft ha realizado una inversión importante en MUI.</span><span class="sxs-lookup"><span data-stu-id="86ca3-120">With Windows Vista, Microsoft made a significant investment in MUI.</span></span> <span data-ttu-id="86ca3-121">Windows Vista se crea desde el principio en una plataforma MUI.</span><span class="sxs-lookup"><span data-stu-id="86ca3-121">Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="86ca3-122">Aunque esto representa un avance importante en la estrategia de localización de Windows, ya que es un componente clave para que Microsoft proporcione Windows en más idiomas que nunca, es primero y más importante para los usuarios y clientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="86ca3-122">While this represents a major advance in Windows localization strategy as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users and customers.</span></span>

### <a name="a-language-neutralmui-operating-system"></a><span data-ttu-id="86ca3-123">Un sistema operativo independiente de idioma o MUI</span><span class="sxs-lookup"><span data-stu-id="86ca3-123">A language neutral/MUI operating system</span></span>

<span data-ttu-id="86ca3-124">La gran mayoría de los binarios de Windows Vista son compatibles con MUI y sus datos localizables se almacenan de forma independiente del código.</span><span class="sxs-lookup"><span data-stu-id="86ca3-124">The vast majority of Windows Vista binaries are MUI compliant, and their localizable data are stored separately from the code.</span></span> <span data-ttu-id="86ca3-125">Esto ofrece flexibilidad, ya que se pueden agregar datos de idioma diferentes en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="86ca3-125">This offers flexibility, as different language data can be added at any time.</span></span>

### <a name="deployment-scenarios-are-fully-mui-based"></a><span data-ttu-id="86ca3-126">Los escenarios de implementación están totalmente basados en MUI</span><span class="sxs-lookup"><span data-stu-id="86ca3-126">Deployment scenarios are fully MUI-based</span></span>

<span data-ttu-id="86ca3-127">El diseño de empaquetado e instalación de Windows Vista se basa en MUI y todos los datos localizables se empaquetan en paquetes específicos del idioma, y cada paquete de idioma se puede implementar en distintos escenarios.</span><span class="sxs-lookup"><span data-stu-id="86ca3-127">The Windows Vista packaging and installation design are MUI-based and all localizable data are packaged in language-specific packs, and each language pack can be deployed in different scenarios.</span></span> <span data-ttu-id="86ca3-128">Por ejemplo, aunque los DVDs comerciales para Windows Vista contienen versiones de un solo idioma, los usuarios de la edición Ultimate pueden descargar paquetes de idioma MUI adicionales y pueden cambiar el idioma de la interfaz de usuario desde el panel de control **configuración regional y de idioma** .</span><span class="sxs-lookup"><span data-stu-id="86ca3-128">For example, although the retail DVDs for Windows Vista contain single-language versions, users of the Ultimate edition can download additional MUI language packs and can switch UI language from the **Regional and Language Options** control panel.</span></span> <span data-ttu-id="86ca3-129">Los licencias de Enterprise Edition obtienen todos los idiomas y pueden implementar cualquiera de ellos.</span><span class="sxs-lookup"><span data-stu-id="86ca3-129">Enterprise edition licensees get all languages and can deploy any of them.</span></span>

### <a name="single-image-deployment"></a><span data-ttu-id="86ca3-130">Implementación de una sola imagen</span><span class="sxs-lookup"><span data-stu-id="86ca3-130">Single image deployment</span></span>

<span data-ttu-id="86ca3-131">Los OEM y los clientes de empresa ahora pueden reducir el número de imágenes que necesitan mantener para implementar Windows y las aplicaciones en equipos en diferentes configuraciones regionales a través de una implementación de imagen única.</span><span class="sxs-lookup"><span data-stu-id="86ca3-131">Enterprise customers and OEMs can now reduce the number of images that they need to maintain in order to deploy Windows and applications onto computers across different locales through single image deployment.</span></span>

<span data-ttu-id="86ca3-132">Con MUI en Windows Vista, se puede implementar una imagen que contenga varios idiomas en cualquier usuario de idioma, y los usuarios pueden determinar sus propios idiomas preferidos (dentro de la Directiva) durante la instalación o la "configuración rápida" del equipo.</span><span class="sxs-lookup"><span data-stu-id="86ca3-132">With MUI on Windows Vista, one image containing multiple languages can be deployed to any language users, and users can determine their own preferred languages (within policy) during setup or initial "out of the box experience" with the computer.</span></span> <span data-ttu-id="86ca3-133">En concreto, los OEM pueden colocar muchos idiomas de interfaz de usuario en sus nuevos equipos para permitir que los usuarios seleccionen uno en el centro de bienvenida.</span><span class="sxs-lookup"><span data-stu-id="86ca3-133">In particular, OEMs can put many UI languages on their new computers to allow users to select one from the Welcome Center.</span></span> <span data-ttu-id="86ca3-134">Por lo tanto, desde una imagen con varios paquetes de idioma, el programa de instalación mostrará una lista de idiomas disponibles y permitirá a los usuarios elegir uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="86ca3-134">Thus, from an image with multiple language packs, Setup will display a list of available languages and enable users to pick one of them.</span></span> <span data-ttu-id="86ca3-135">Toda la configuración internacional se establece para que coincida con el idioma o la configuración regional seleccionados.</span><span class="sxs-lookup"><span data-stu-id="86ca3-135">All international settings are then set to match the selected language or locale.</span></span>

### <a name="improved-servicing-model"></a><span data-ttu-id="86ca3-136">Modelo de servicio mejorado</span><span class="sxs-lookup"><span data-stu-id="86ca3-136">Improved servicing model</span></span>

<span data-ttu-id="86ca3-137">El mismo paquete QFE o corrección de seguridad ahora se puede instalar sobre cualquier sistema de idioma.</span><span class="sxs-lookup"><span data-stu-id="86ca3-137">The same QFE or security fix package can now be installed on top of any language systems.</span></span> <span data-ttu-id="86ca3-138">Esto es fundamental, ya que permite un procesamiento más rápido de las correcciones de seguridad en particular y permite a todos los usuarios internacionales beneficiarse de la misma disponibilidad de todas las correcciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="86ca3-138">This is critical as it enables a faster turnaround of security fixes in particular and enables all international users to benefit from the same time availability of all security fixes.</span></span>

### <a name="mui-infrastructure"></a><span data-ttu-id="86ca3-139">Infraestructura de MUI</span><span class="sxs-lookup"><span data-stu-id="86ca3-139">MUI infrastructure</span></span>

<span data-ttu-id="86ca3-140">A partir de Windows Vista, las API de MUI están disponibles para que los desarrolladores puedan aprovechar las ventajas de los mecanismos de MUI para sus propias aplicaciones, sin tener que crear lógica personalizada para la administración de recursos y el control de los recursos.</span><span class="sxs-lookup"><span data-stu-id="86ca3-140">Starting with Windows Vista, MUI APIs are available to enable developers to take advantage of the MUI mechanisms for their own applications, without having to create custom logic for resource handling and language management.</span></span>

### <a name="language-management"></a><span data-ttu-id="86ca3-141">Administración de idiomas</span><span class="sxs-lookup"><span data-stu-id="86ca3-141">Language management</span></span>

<span data-ttu-id="86ca3-142">Las API de MUI de base que proporcionan capacidades de administración del idioma de la interfaz de usuario están disponibles como parte de la infraestructura de MUI.</span><span class="sxs-lookup"><span data-stu-id="86ca3-142">Base MUI APIs that provide UI language management capabilities are available as part of the MUI infrastructure.</span></span> <span data-ttu-id="86ca3-143">Para ayudar a administrar la configuración de idioma de interfaz de usuario diferente en el nivel de sistema, usuario y aplicación, MUI los combina internamente en una sola lista de prioridades.</span><span class="sxs-lookup"><span data-stu-id="86ca3-143">To help manage the different UI language settings at the system, user, and application level, MUI internally combines them into a single prioritized list.</span></span> <span data-ttu-id="86ca3-144">A continuación, MUI implementa un mecanismo de reserva basado en esta lista priorizada, lo que permite soluciones de localización parciales a la vez que se proporciona a los usuarios una experiencia de idioma de interfaz de usuario adecuada (si no se prefiere).</span><span class="sxs-lookup"><span data-stu-id="86ca3-144">MUI then implements a fallback mechanism based on this prioritized list, allowing for partial localization solutions while providing users with an appropriate—if not preferred—user interface language experience.</span></span>

<span data-ttu-id="86ca3-145">Por ejemplo, un sistema que ejecuta la versión en Español de Windows Vista con un paquete de interfaz de idiomas (LIP) de catalán instalado sobre el sistema operativo base puede admitir el comportamiento siguiente: el sistema probará y mostrará primero sus recursos en catalán, y si estos recursos no están disponibles en catalán, proporcione en su lugar el usuario con recursos en español.</span><span class="sxs-lookup"><span data-stu-id="86ca3-145">For example, a system running the Spanish version of Windows Vista with a Catalan language interface pack (LIP) installed on top of the base operating system can support the following behavior: the system will try and display its resources in Catalan first, and if these resources are not available in Catalan, then provide the user with Spanish resources instead.</span></span>

### <a name="resource-handling"></a><span data-ttu-id="86ca3-146">Administración de recursos</span><span class="sxs-lookup"><span data-stu-id="86ca3-146">Resource handling</span></span>

<span data-ttu-id="86ca3-147">Con la infraestructura de MUI mejorada que está disponible a partir de Windows Vista, la mayoría de las tecnologías de recursos comunes están habilitadas para MUI.</span><span class="sxs-lookup"><span data-stu-id="86ca3-147">With the improved MUI infrastructure that is available starting with Windows Vista, most common resource technologies are MUI-enabled.</span></span> <span data-ttu-id="86ca3-148">En la tabla siguiente se proporcionan detalles adicionales sobre la compatibilidad con el control de recursos disponible en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="86ca3-148">The following table provides additional details on the resource handling support available in Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="86ca3-149">Category</span><span class="sxs-lookup"><span data-stu-id="86ca3-149">Category</span></span></th>
<th><span data-ttu-id="86ca3-150">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="86ca3-150">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="86ca3-151">Tipos de recurso admitidos</span><span class="sxs-lookup"><span data-stu-id="86ca3-151">Supported resource types</span></span></td>
<td><ul>
<li><span data-ttu-id="86ca3-152">Win32/recurso no administrado:. DLL/. EXE/. OCX</span><span class="sxs-lookup"><span data-stu-id="86ca3-152">Win32/unmanaged resource: .DLL/.EXE/.OCX</span></span></li>
<li><span data-ttu-id="86ca3-153">Registros relacionados con el shell</span><span class="sxs-lookup"><span data-stu-id="86ca3-153">Shell-related registrations</span></span></li>
<li><span data-ttu-id="86ca3-154">Recursos relacionados con la administración: registro de eventos, Complementos/archivos MSC</span><span class="sxs-lookup"><span data-stu-id="86ca3-154">Management-related resources: Event log, Snap-in/MSC files</span></span></li>
<li><span data-ttu-id="86ca3-155">WMI: MOF/MFL</span><span class="sxs-lookup"><span data-stu-id="86ca3-155">WMI: MOF/MFL</span></span></li>
<li><span data-ttu-id="86ca3-156">Directiva de grupo: ADMX/ADML</span><span class="sxs-lookup"><span data-stu-id="86ca3-156">Group Policy: ADMX/ADML</span></span></li>
<li><span data-ttu-id="86ca3-157">Resources.dll administrado</span><span class="sxs-lookup"><span data-stu-id="86ca3-157">Managed Resources.dll</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="86ca3-158">Herramientas de desarrollo</span><span class="sxs-lookup"><span data-stu-id="86ca3-158">Development Tools</span></span></td>
<td><ul>
<li><span data-ttu-id="86ca3-159">Para Win32: RC.exe, MUIRCT.exe y Visual Studio 2005 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="86ca3-159">For Win32: RC.exe, MUIRCT.exe and Visual Studio 2005 and later</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="86ca3-160">Compatibilidad con tipos de recursos limitados</span><span class="sxs-lookup"><span data-stu-id="86ca3-160">Limited resource type support</span></span></td>
<td><ul>
<li><span data-ttu-id="86ca3-161">archivos de ayuda \*. chm</span><span class="sxs-lookup"><span data-stu-id="86ca3-161">\*.chm help files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



