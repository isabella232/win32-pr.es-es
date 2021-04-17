---
description: Msitran.exe usa MsiDatabaseGenerateTransform, MsiCreateTransformSummaryInfo y MsiDatabaseApplyTransform para generar o aplicar un archivo de transformación. Esta herramienta solo está disponible en los componentes de Windows SDK para los desarrolladores de Windows Installer.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69936155fb3880f43e0f7563bc6aabd59f53703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678248"
---
# <a name="msitranexe"></a><span data-ttu-id="7ebd3-103">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="7ebd3-103">Msitran.exe</span></span>

<span data-ttu-id="7ebd3-104">Msitran.exe usa [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)y [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) para generar o aplicar un archivo de transformación.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-104">Msitran.exe uses [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa), and [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) to generate or apply a transform file.</span></span>

<span data-ttu-id="7ebd3-105">Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="7ebd3-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7ebd3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ebd3-106">Syntax</span></span>

<span data-ttu-id="7ebd3-107">Use la siguiente sintaxis para generar una transformación.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-107">Use the following syntax to generate a transform.</span></span>

<span data-ttu-id="7ebd3-108">**MsiTran-g** *{base dB} {Ref dB} {Transform File name} \[ {condiciones de error/condiciones de \] validación}*</span><span class="sxs-lookup"><span data-stu-id="7ebd3-108">**msitran -g** *{base db}{ref db}{transform file name}\[{error conditions / validation conditions}\]*</span></span>

<span data-ttu-id="7ebd3-109">Use la siguiente sintaxis para aplicar una transformación</span><span class="sxs-lookup"><span data-stu-id="7ebd3-109">Use the following syntax to apply a transform</span></span>

<span data-ttu-id="7ebd3-110">**MsiTran-a** *{Transform} {Database} \[ {condiciones de error \] }*</span><span class="sxs-lookup"><span data-stu-id="7ebd3-110">**msitran -a** *{transform}{database}\[{error conditions}\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="7ebd3-111">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="7ebd3-111">Command Line Options</span></span>

<span data-ttu-id="7ebd3-112">Msitran.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-112">Msitran.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="7ebd3-113">También se puede usar un delimitador de barra diagonal en lugar de un guión.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="7ebd3-114">Opción</span><span class="sxs-lookup"><span data-stu-id="7ebd3-114">Option</span></span> | <span data-ttu-id="7ebd3-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ebd3-115">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="7ebd3-116">-g</span><span class="sxs-lookup"><span data-stu-id="7ebd3-116">-g</span></span>     | <span data-ttu-id="7ebd3-117">Generación de transformación.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-117">Transform generation.</span></span>  |
| <span data-ttu-id="7ebd3-118">-a</span><span class="sxs-lookup"><span data-stu-id="7ebd3-118">-a</span></span>     | <span data-ttu-id="7ebd3-119">Aplicación de transformación.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-119">Transform application.</span></span> |



 

<span data-ttu-id="7ebd3-120">Los errores siguientes se pueden suprimir al aplicar una transformación.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-120">The following errors may be suppressed when applying a transform.</span></span> <span data-ttu-id="7ebd3-121">Para suprimir un error, incluya el carácter apropiado en el argumento {error conditions}.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-121">To suppress an error, include the appropriate character in the {error conditions} argument.</span></span> <span data-ttu-id="7ebd3-122">Las condiciones especificadas con-g se colocan en la información de Resumen de la transformación, pero no se usan al aplicar una transformación con-a.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-122">Conditions specified with -g are placed in the summary information of the transform, but are not used when applying a transform with -a.</span></span> <span data-ttu-id="7ebd3-123">Para obtener información, consulte [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).</span><span class="sxs-lookup"><span data-stu-id="7ebd3-123">For information, see [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).</span></span>



| <span data-ttu-id="7ebd3-124">Opción</span><span class="sxs-lookup"><span data-stu-id="7ebd3-124">Option</span></span> | <span data-ttu-id="7ebd3-125">Error suprimido</span><span class="sxs-lookup"><span data-stu-id="7ebd3-125">Suppressed error</span></span>           |
|--------|----------------------------|
| <span data-ttu-id="7ebd3-126">a</span><span class="sxs-lookup"><span data-stu-id="7ebd3-126">a</span></span>      | <span data-ttu-id="7ebd3-127">Agregar fila existente.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-127">Add existing row.</span></span>          |
| <span data-ttu-id="7ebd3-128">b</span><span class="sxs-lookup"><span data-stu-id="7ebd3-128">b</span></span>      | <span data-ttu-id="7ebd3-129">Elimina una fila no existente.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-129">Delete non-existing row.</span></span>   |
| <span data-ttu-id="7ebd3-130">c</span><span class="sxs-lookup"><span data-stu-id="7ebd3-130">c</span></span>      | <span data-ttu-id="7ebd3-131">Agregar tabla existente.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-131">Add existing table.</span></span>        |
| <span data-ttu-id="7ebd3-132">d</span><span class="sxs-lookup"><span data-stu-id="7ebd3-132">d</span></span>      | <span data-ttu-id="7ebd3-133">Eliminar tabla no existente.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-133">Delete non-existing table.</span></span> |
| <span data-ttu-id="7ebd3-134">h</span><span class="sxs-lookup"><span data-stu-id="7ebd3-134">e</span></span>      | <span data-ttu-id="7ebd3-135">Modifique la fila existente.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-135">Modify existing row.</span></span>       |
| <span data-ttu-id="7ebd3-136">f</span><span class="sxs-lookup"><span data-stu-id="7ebd3-136">f</span></span>      | <span data-ttu-id="7ebd3-137">Cambiar página de códigos.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-137">Change codepage.</span></span>           |



 

<span data-ttu-id="7ebd3-138">Se pueden usar las siguientes condiciones de validación para indicar cuándo se puede aplicar una transformación a un paquete.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-138">The following validation conditions may be used to indicate when a transform may be applied to a package.</span></span> <span data-ttu-id="7ebd3-139">Estas condiciones se pueden especificar con-g, pero no con-a.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-139">These conditions may be specified with -g, but not -a.</span></span>



| <span data-ttu-id="7ebd3-140">Opción</span><span class="sxs-lookup"><span data-stu-id="7ebd3-140">Option</span></span> | <span data-ttu-id="7ebd3-141">Condición de validación</span><span class="sxs-lookup"><span data-stu-id="7ebd3-141">Validation condition</span></span>                                  |
|--------|-------------------------------------------------------|
| <span data-ttu-id="7ebd3-142">e</span><span class="sxs-lookup"><span data-stu-id="7ebd3-142">g</span></span>      | <span data-ttu-id="7ebd3-143">Compruebe el código de actualización.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-143">Check upgrade code.</span></span>                                   |
| <span data-ttu-id="7ebd3-144">l</span><span class="sxs-lookup"><span data-stu-id="7ebd3-144">l</span></span>      | <span data-ttu-id="7ebd3-145">Compruebe el idioma.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-145">Check language.</span></span>                                       |
| <span data-ttu-id="7ebd3-146">p</span><span class="sxs-lookup"><span data-stu-id="7ebd3-146">p</span></span>      | <span data-ttu-id="7ebd3-147">Compruebe la plataforma.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-147">Check platform.</span></span>                                       |
| <span data-ttu-id="7ebd3-148">r</span><span class="sxs-lookup"><span data-stu-id="7ebd3-148">r</span></span>      | <span data-ttu-id="7ebd3-149">Compruebe el producto.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-149">Check product.</span></span>                                        |
| <span data-ttu-id="7ebd3-150">s</span><span class="sxs-lookup"><span data-stu-id="7ebd3-150">s</span></span>      | <span data-ttu-id="7ebd3-151">Compruebe solo la versión principal.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-151">Check major version only.</span></span>                             |
| <span data-ttu-id="7ebd3-152">t</span><span class="sxs-lookup"><span data-stu-id="7ebd3-152">t</span></span>      | <span data-ttu-id="7ebd3-153">Compruebe solo las versiones principal y secundaria.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-153">Check major and minor versions only.</span></span>                  |
| <span data-ttu-id="7ebd3-154">u</span><span class="sxs-lookup"><span data-stu-id="7ebd3-154">u</span></span>      | <span data-ttu-id="7ebd3-155">Compruebe las versiones principal, secundaria y de actualización.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-155">Check major, minor, and upgrade versions.</span></span>             |
| <span data-ttu-id="7ebd3-156">v</span><span class="sxs-lookup"><span data-stu-id="7ebd3-156">v</span></span>      | <span data-ttu-id="7ebd3-157">Versión de base de datos aplicada < versión de base de datos base.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-157">Applied database version < Base database version.</span></span>  |
| <span data-ttu-id="7ebd3-158">w</span><span class="sxs-lookup"><span data-stu-id="7ebd3-158">w</span></span>      | <span data-ttu-id="7ebd3-159">Versión de base de datos aplicada <= versión de base de datos base.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-159">Applied database version <= Base database version.</span></span> |
| <span data-ttu-id="7ebd3-160">x</span><span class="sxs-lookup"><span data-stu-id="7ebd3-160">x</span></span>      | <span data-ttu-id="7ebd3-161">Versión de base de datos aplicada = versión de base de datos base.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-161">Applied database version = Base database version.</span></span>     |
| <span data-ttu-id="7ebd3-162">y</span><span class="sxs-lookup"><span data-stu-id="7ebd3-162">y</span></span>      | <span data-ttu-id="7ebd3-163">Versión de base de datos aplicada >= versión de base de datos base.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-163">Applied database version >= Base database version.</span></span> |
| <span data-ttu-id="7ebd3-164">z</span><span class="sxs-lookup"><span data-stu-id="7ebd3-164">z</span></span>      | <span data-ttu-id="7ebd3-165">Versión de base de datos aplicada > versión de base de datos base.</span><span class="sxs-lookup"><span data-stu-id="7ebd3-165">Applied database version > Base database version.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="7ebd3-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7ebd3-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ebd3-167">Herramientas de desarrollo de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="7ebd3-167">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="7ebd3-168">Transformaciones de base de datos</span><span class="sxs-lookup"><span data-stu-id="7ebd3-168">Database Transforms</span></span>](database-transforms.md)
</dt> <dt>

[<span data-ttu-id="7ebd3-169">Ejemplo de transformación de personalización</span><span class="sxs-lookup"><span data-stu-id="7ebd3-169">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> <dt>

[<span data-ttu-id="7ebd3-170">Versiones publicadas, herramientas y redistribuibles</span><span class="sxs-lookup"><span data-stu-id="7ebd3-170">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



