---
description: En el caso de un paquete de instalación, la propiedad de Resumen de la plantilla indica las versiones de plataforma y de idioma que son compatibles con esta base de datos de instalación.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Propiedad de Resumen de plantilla
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b3949e7028fd0b1b5f9ff3112f1a3d03c9b87e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679281"
---
# <a name="template-summary-property"></a><span data-ttu-id="84aa8-103">Propiedad de Resumen de plantilla</span><span class="sxs-lookup"><span data-stu-id="84aa8-103">Template Summary property</span></span>

<span data-ttu-id="84aa8-104">En el caso de un paquete de instalación, la propiedad de Resumen de la **plantilla** indica las versiones de plataforma y de idioma que son compatibles con esta base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="84aa8-104">For an installation package, the **Template Summary** property indicates the platform and language versions that are compatible with this installation database.</span></span> <span data-ttu-id="84aa8-105">La sintaxis de la información de la propiedad de Resumen de la **plantilla** para una base de datos de instalación es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="84aa8-105">The syntax of the **Template Summary** property information for an installation database is the following:</span></span>

<span data-ttu-id="84aa8-106">\[*propiedad Platform* \] ; \[ *identificador* \] \[ de idioma,,... de *identificador de idioma* \] \[ \] .</span><span class="sxs-lookup"><span data-stu-id="84aa8-106">\[*platform property*\];\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="84aa8-107">Los ejemplos siguientes son valores válidos para la propiedad de **Resumen de plantilla** :</span><span class="sxs-lookup"><span data-stu-id="84aa8-107">The following examples are valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="84aa8-108">x64; 1033</span><span class="sxs-lookup"><span data-stu-id="84aa8-108">x64;1033</span></span>
-   <span data-ttu-id="84aa8-109">Intel; 1033</span><span class="sxs-lookup"><span data-stu-id="84aa8-109">Intel;1033</span></span>
-   <span data-ttu-id="84aa8-110">Intel64; 1033</span><span class="sxs-lookup"><span data-stu-id="84aa8-110">Intel64;1033</span></span>
-   <span data-ttu-id="84aa8-111">; 1033</span><span class="sxs-lookup"><span data-stu-id="84aa8-111">;1033</span></span>
-   <span data-ttu-id="84aa8-112">Intel; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="84aa8-112">Intel ;1033,2046</span></span>
-   <span data-ttu-id="84aa8-113">Intel64; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="84aa8-113">Intel64;1033,2046</span></span>
-   <span data-ttu-id="84aa8-114">Intel; 0</span><span class="sxs-lookup"><span data-stu-id="84aa8-114">Intel;0</span></span>
-   <span data-ttu-id="84aa8-115">ARM; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="84aa8-115">Arm;1033,2046</span></span>
-   <span data-ttu-id="84aa8-116">ARM; 0</span><span class="sxs-lookup"><span data-stu-id="84aa8-116">Arm;0</span></span>
-   <span data-ttu-id="84aa8-117">Arm64; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="84aa8-117">Arm64;1033,2046</span></span>
-   <span data-ttu-id="84aa8-118">Arm64; 0</span><span class="sxs-lookup"><span data-stu-id="84aa8-118">Arm64;0</span></span>

<span data-ttu-id="84aa8-119">La propiedad **Resumen de plantilla** de una transformación indica las versiones de plataforma y de idioma compatibles con la transformación.</span><span class="sxs-lookup"><span data-stu-id="84aa8-119">The **Template Summary** property of a transform indicates the platform and language versions compatible with the transform.</span></span> <span data-ttu-id="84aa8-120">En un archivo de transformación, solo se puede especificar un idioma.</span><span class="sxs-lookup"><span data-stu-id="84aa8-120">In a transform file, only one language may be specified.</span></span> <span data-ttu-id="84aa8-121">La plataforma y el idioma especificados determinan si una transformación puede aplicarse a una base de datos determinada.</span><span class="sxs-lookup"><span data-stu-id="84aa8-121">The specified platform and language determine whether a transform can be applied to a particular database.</span></span> <span data-ttu-id="84aa8-122">La propiedad Platform y la propiedad Language se pueden dejar en blanco si no se basa ninguna restricción de transformación para validar la transformación.</span><span class="sxs-lookup"><span data-stu-id="84aa8-122">The platform property and the language property can be left blank if no transform restriction relies on them to validate the transform.</span></span>

<span data-ttu-id="84aa8-123">La propiedad de **Resumen de plantilla** de un paquete de revisión es una lista delimitada por signos de punto y coma de los códigos de producto que pueden aceptar la revisión.</span><span class="sxs-lookup"><span data-stu-id="84aa8-123">The **Template Summary** property of a patch package is a semicolon-delimited list of the product codes that can accept the patch.</span></span> <span data-ttu-id="84aa8-124">Si utiliza [Msimsp.exe](msimsp-exe.md) y [Patchwiz.dll](patchwiz-dll.md) para generar el paquete de revisión, esta lista se obtiene de la [tabla TargetImages](targetimages-table-patchwiz-dll-.md) del archivo de creación de la revisión.</span><span class="sxs-lookup"><span data-stu-id="84aa8-124">If you use [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate the patch package, this list is obtained from the [TargetImages table](targetimages-table-patchwiz-dll-.md) of the patch creation file.</span></span>

<span data-ttu-id="84aa8-125">Esta propiedad de resumen es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="84aa8-125">This summary property is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="84aa8-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84aa8-126">Remarks</span></span>

<span data-ttu-id="84aa8-127">Si la plataforma actual no coincide con una de las plataformas especificadas en la propiedad de **Resumen de plantilla** , el instalador no procesa el paquete.</span><span class="sxs-lookup"><span data-stu-id="84aa8-127">If the current platform does not match one of the platforms specified in the **Template Summary** property then the installer does not process the package.</span></span>

<span data-ttu-id="84aa8-128">Si falta la especificación de la plataforma en el valor de propiedad de Resumen de la **plantilla** , el instalador asume la arquitectura de Intel.</span><span class="sxs-lookup"><span data-stu-id="84aa8-128">If the platform specification is missing in the **Template Summary** property value, the installer assumes the Intel architecture.</span></span>

<span data-ttu-id="84aa8-129">Si se trata de un paquete de Windows Installer de 64 bits que se ejecuta en una plataforma Intel64 (Itanium), escriba Intel64 en la propiedad Resumen de la **plantilla** .</span><span class="sxs-lookup"><span data-stu-id="84aa8-129">If this is a 64-bit Windows Installer package being run on an Intel64 (Itanium) platform, enter Intel64 in the **Template Summary** property.</span></span>

<span data-ttu-id="84aa8-130">Si se trata de un paquete de Windows Installer de 64 bits que se ejecuta en una plataforma x64, escriba x64 en la propiedad Resumen de la **plantilla** .</span><span class="sxs-lookup"><span data-stu-id="84aa8-130">If this is a 64-bit Windows Installer package being run on a x64 platform, enter x64 in the **Template Summary** property.</span></span>

<span data-ttu-id="84aa8-131">Si se trata de un paquete de Windows Installer de 64 bits que se ejecuta en una plataforma Arm64, escriba Arm64 en la propiedad Resumen de la **plantilla** .</span><span class="sxs-lookup"><span data-stu-id="84aa8-131">If this is a 64-bit Windows Installer package being run on an Arm64 platform, enter Arm64 in the **Template Summary** property.</span></span>

<span data-ttu-id="84aa8-132">No se puede marcar un paquete de Windows Installer como compatible con Intel64 y x64; por ejemplo, el valor de la propiedad Summary de la **plantilla** de Intel64, x64 no es válido.</span><span class="sxs-lookup"><span data-stu-id="84aa8-132">A Windows Installer package cannot be marked as supporting both Intel64 and x64; for example, the **Template Summary** property value of Intel64,x64 is invalid.</span></span>

<span data-ttu-id="84aa8-133">No se puede marcar un paquete de Windows Installer como compatible con plataformas de 32 bits y de 64 bits; por ejemplo, los valores de propiedad de **Resumen de plantilla** como Intel, x64 o Intel, Intel64 no son válidos.</span><span class="sxs-lookup"><span data-stu-id="84aa8-133">A Windows Installer package cannot be marked as supporting both 32-bit and 64-bit platforms; for example, **Template Summary** property values such as Intel,x64 or Intel,Intel64 are invalid.</span></span>

<span data-ttu-id="84aa8-134">Si escribe 0 (cero) en el campo ID. de idioma de la propiedad Resumen de la **plantilla** o si se mantiene este campo vacío, indica que el paquete es independiente del idioma.</span><span class="sxs-lookup"><span data-stu-id="84aa8-134">Entering 0 (zero) in the language ID field of the **Template Summary** property, or leaving this field empty, indicates that the package is language neutral.</span></span>

<span data-ttu-id="84aa8-135">Si se trata de un paquete de Windows Installer que se ejecuta en Windows RT, escriba el valor ARM en la propiedad de Resumen de la **plantilla** .</span><span class="sxs-lookup"><span data-stu-id="84aa8-135">If this is a Windows Installer package being run on Windows RT, enter the value Arm in the **Template Summary** property.</span></span>

<span data-ttu-id="84aa8-136">Los módulos de fusión mediante combinación son los únicos paquetes que pueden tener varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="84aa8-136">Merge Modules are the only packages that may have multiple languages.</span></span> <span data-ttu-id="84aa8-137">Solo se puede especificar un idioma en una base de datos del instalador de origen.</span><span class="sxs-lookup"><span data-stu-id="84aa8-137">Only one language can be specified in a source installer database.</span></span> <span data-ttu-id="84aa8-138">Para obtener más información, vea [módulos de combinación en varios idiomas](multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="84aa8-138">For more information, see [Multiple Language Merge Modules](multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="84aa8-139">La plataforma Alpha no es compatible con Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="84aa8-139">The Alpha platform is not supported by Windows Installer.</span></span>

<span data-ttu-id="84aa8-140">**Windows Installer:** No se admite la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="84aa8-140">**Windows Installer:** The following syntax is not supported:</span></span>

<span data-ttu-id="84aa8-141">\[*propiedad Platform* \] \[ ,*propiedad Platform* \] \[ \] ,... \[ *identificador* \] \[ de idioma,,... de *identificador de idioma* \] \[ \] .</span><span class="sxs-lookup"><span data-stu-id="84aa8-141">\[*platform property*\]\[,*platform property*\]\[,...\]\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="84aa8-142">Los ejemplos siguientes no son valores válidos para la propiedad de **Resumen de plantilla** :</span><span class="sxs-lookup"><span data-stu-id="84aa8-142">The following examples are not valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="84aa8-143">Alpha, Intel; 1033</span><span class="sxs-lookup"><span data-stu-id="84aa8-143">Alpha,Intel;1033</span></span>
-   <span data-ttu-id="84aa8-144">Intel, Alpha; 1033</span><span class="sxs-lookup"><span data-stu-id="84aa8-144">Intel,Alpha;1033</span></span>
-   <span data-ttu-id="84aa8-145">Alfa; 1033</span><span class="sxs-lookup"><span data-stu-id="84aa8-145">Alpha;1033</span></span>
-   <span data-ttu-id="84aa8-146">Alpha; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="84aa8-146">Alpha;1033,2046</span></span>

## <a name="requirements"></a><span data-ttu-id="84aa8-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84aa8-147">Requirements</span></span>



| <span data-ttu-id="84aa8-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="84aa8-148">Requirement</span></span> | <span data-ttu-id="84aa8-149">Value</span><span class="sxs-lookup"><span data-stu-id="84aa8-149">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84aa8-150">Versión</span><span class="sxs-lookup"><span data-stu-id="84aa8-150">Version</span></span><br/> | <span data-ttu-id="84aa8-151">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="84aa8-151">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="84aa8-152">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="84aa8-152">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="84aa8-153">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa8-153">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84aa8-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="84aa8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84aa8-155">Descripciones de propiedades de Resumen</span><span class="sxs-lookup"><span data-stu-id="84aa8-155">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




