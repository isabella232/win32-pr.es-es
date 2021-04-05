---
description: Una instalación administrativa crea una imagen de origen de una aplicación o un producto en una red.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Aplicar actualizaciones pequeñas mediante la revisión de una imagen administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dad22d91e101d79d2bf6ecc0efc8ea9358eda2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001748"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a><span data-ttu-id="c6a39-103">Aplicar actualizaciones pequeñas mediante la revisión de una imagen administrativa</span><span class="sxs-lookup"><span data-stu-id="c6a39-103">Applying Small Updates by Patching an Administrative Image</span></span>

<span data-ttu-id="c6a39-104">Una [instalación administrativa](administrative-installation.md) crea una imagen de origen de una aplicación o un producto en una red.</span><span class="sxs-lookup"><span data-stu-id="c6a39-104">An [administrative installation](administrative-installation.md) creates a source image of an application or product on a network.</span></span> <span data-ttu-id="c6a39-105">Los usuarios de un grupo de trabajo que tengan acceso a esta imagen administrativa pueden instalar el producto desde este origen.</span><span class="sxs-lookup"><span data-stu-id="c6a39-105">Users in a workgroup who have access to this administrative image can install the product from this source.</span></span> <span data-ttu-id="c6a39-106">La actualización de la aplicación para este grupo de trabajo se realiza en dos pasos:</span><span class="sxs-lookup"><span data-stu-id="c6a39-106">Updating the application for this workgroup is done in two steps:</span></span>

-   <span data-ttu-id="c6a39-107">En primer lugar, se puede aplicar la revisión de actualización pequeña a la imagen administrativa.</span><span class="sxs-lookup"><span data-stu-id="c6a39-107">First, the small update patch can be applied to the administrative image.</span></span>
-   <span data-ttu-id="c6a39-108">En segundo lugar, los cambios en la actualización pequeña deben propagarse a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="c6a39-108">Second, the changes in the small update need to be propagated to the users.</span></span>

<span data-ttu-id="c6a39-109">**Para aplicar una pequeña revisión de actualización a una imagen administrativa**</span><span class="sxs-lookup"><span data-stu-id="c6a39-109">**To apply a small update patch to an administrative image**</span></span>

1.  <span data-ttu-id="c6a39-110">Obtenga la actualización pequeña en forma de paquete de [revisión](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="c6a39-110">Obtain the small update in the form of a [patch package](patch-packages.md).</span></span> <span data-ttu-id="c6a39-111">Por ejemplo, la actualización pequeña denominada patch. msp.</span><span class="sxs-lookup"><span data-stu-id="c6a39-111">For example, the small update named Patch.msp.</span></span>
2.  <span data-ttu-id="c6a39-112">Obtenga la ruta de acceso a la imagen administrativa.</span><span class="sxs-lookup"><span data-stu-id="c6a39-112">Obtain the path to the administrative image.</span></span>
3.  <span data-ttu-id="c6a39-113">En la línea de comandos, use:</span><span class="sxs-lookup"><span data-stu-id="c6a39-113">From the command line use:</span></span>

    <span data-ttu-id="c6a39-114">**msiexec/a** *\[ ruta de acceso al archivo \] . msi de la imagen administrativa* **/p** *patch. MSP*</span><span class="sxs-lookup"><span data-stu-id="c6a39-114">**msiexec /a** *\[path to administrative image .msi file\]* **/p** *patch.msp*</span></span>

4.  <span data-ttu-id="c6a39-115">De esta forma se actualizan los archivos de aplicación y el archivo. msi de la imagen administrativa.</span><span class="sxs-lookup"><span data-stu-id="c6a39-115">This updates the application files and the .msi file of the administrative image.</span></span> <span data-ttu-id="c6a39-116">Para obtener una lista de las opciones que se pueden utilizar con Msiexec.exe, vea opciones de la [línea de comandos](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="c6a39-116">For a list of the options that can be used with Msiexec.exe, see [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="c6a39-117">Windows Installer determina automáticamente si la imagen administrativa usa nombres de archivo cortos y establece la propiedad [**SHORTFILENAMES**](shortfilenames.md) .</span><span class="sxs-lookup"><span data-stu-id="c6a39-117">Windows Installer automatically determines whether the administrative image is using short file names and sets the [**SHORTFILENAMES**](shortfilenames.md) property.</span></span>
5.  <span data-ttu-id="c6a39-118">La imagen administrativa resultante es la misma que la generada por una instalación administrativa con un CD-ROM completo del producto que incluye la actualización.</span><span class="sxs-lookup"><span data-stu-id="c6a39-118">The resulting administrative image is the same as that produced by an administrative installation using a full product CD-ROM that includes the update.</span></span> <span data-ttu-id="c6a39-119">Cuando los nuevos usuarios instalan la aplicación desde este origen, reciben la aplicación actualizada.</span><span class="sxs-lookup"><span data-stu-id="c6a39-119">When new users install the application from this source they receive the updated application.</span></span>

<span data-ttu-id="c6a39-120">**Para propagar la pequeña actualización al grupo de trabajo**</span><span class="sxs-lookup"><span data-stu-id="c6a39-120">**To propagate the small update to the workgroup**</span></span>

-   <span data-ttu-id="c6a39-121">Los miembros del grupo de trabajo obtienen los cambios reinstalando la aplicación a partir de la imagen administrativa mediante el procedimiento descrito en [aplicación de actualizaciones pequeñas reinstalando el producto](applying-small-updates-by-reinstalling-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="c6a39-121">Members of the workgroup obtain the changes by reinstalling the application from the administrative image using the procedure described in [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md).</span></span>

 

 



