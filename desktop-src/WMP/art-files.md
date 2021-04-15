---
title: Archivos de imagen
description: Archivos de imagen
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Aspectos de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a246ac411a3dfe2c5bab529ddcccce5596434617
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695460"
---
# <a name="art-files"></a><span data-ttu-id="16940-107">Archivos de imagen</span><span class="sxs-lookup"><span data-stu-id="16940-107">Art Files</span></span>

<span data-ttu-id="16940-108">Debe crear uno o varios archivos de imagen para la máscara.</span><span class="sxs-lookup"><span data-stu-id="16940-108">You must create one or more art files for your skin.</span></span> <span data-ttu-id="16940-109">Sin arte, el usuario no tendrá nada que ver.</span><span class="sxs-lookup"><span data-stu-id="16940-109">Without art, the user will have nothing to look at.</span></span> <span data-ttu-id="16940-110">Podría crear una máscara invisible, pero nadie la verá.</span><span class="sxs-lookup"><span data-stu-id="16940-110">You could create an invisible skin, but no one would see it!</span></span> <span data-ttu-id="16940-111">E incluso después, todavía tendría que crear archivos de imagen para almacenar las imágenes invisibles, ya que el archivo de definición de máscara requiere archivos de imagen para elementos específicos.</span><span class="sxs-lookup"><span data-stu-id="16940-111">And even then, you would still have to create art files to hold your invisible images, because the skin definition file requires art files for specific elements.</span></span>

<span data-ttu-id="16940-112">Hay tres usos para las ilustraciones en las máscaras: imágenes principales, imágenes de asignación e imágenes alternativas.</span><span class="sxs-lookup"><span data-stu-id="16940-112">There are three uses for art in skins: primary images, mapping images, and alternate images.</span></span>

## <a name="primary-images"></a><span data-ttu-id="16940-113">Imágenes principales</span><span class="sxs-lookup"><span data-stu-id="16940-113">Primary Images</span></span>

<span data-ttu-id="16940-114">Debe crear una imagen primaria para la máscara.</span><span class="sxs-lookup"><span data-stu-id="16940-114">You must create a primary image for your skin.</span></span> <span data-ttu-id="16940-115">Esto es lo que verán los usuarios cuando instalen la máscara.</span><span class="sxs-lookup"><span data-stu-id="16940-115">This is what the users will see when they install your skin.</span></span> <span data-ttu-id="16940-116">La imagen principal se compone de una o varias imágenes que se crean mediante controles de máscara concretos.</span><span class="sxs-lookup"><span data-stu-id="16940-116">The primary image is composed of one or more images that are created by specific skin controls.</span></span>

<span data-ttu-id="16940-117">Si tiene más de un control, debe especificar el orden z, que define los controles que se muestran delante de otros controles.</span><span class="sxs-lookup"><span data-stu-id="16940-117">If you have more than one control, you must specify the z-order, which defines which controls are displayed in front of other controls.</span></span> <span data-ttu-id="16940-118">Cada elemento de **vista** tendrá una imagen de fondo a la que puede agregar otras imágenes de elementos, lo que le permitirá crear una imagen compuesta principal.</span><span class="sxs-lookup"><span data-stu-id="16940-118">Each **View** element will have a background image that you can add other element images to, allowing you to create a primary composite image.</span></span>

<span data-ttu-id="16940-119">También puede tener imágenes secundarias, como una bandeja deslizante, que no se muestran cuando se muestra la máscara por primera vez, pero que se muestran cuando el usuario realiza alguna acción.</span><span class="sxs-lookup"><span data-stu-id="16940-119">You also may have secondary images, such as a sliding tray, that do not display when your skin first appears, but that show up when the user takes some action.</span></span> <span data-ttu-id="16940-120">Estos siguen las mismas reglas que las imágenes principales, ya que se crean con un conjunto de controles.</span><span class="sxs-lookup"><span data-stu-id="16940-120">These follow the same rules as primary images, in that they are created with a set of controls.</span></span>

## <a name="mapping-images"></a><span data-ttu-id="16940-121">Asignar imágenes</span><span class="sxs-lookup"><span data-stu-id="16940-121">Mapping Images</span></span>

<span data-ttu-id="16940-122">Una de las características más eficaces de las máscaras de Windows Media Player es que puede usar la asignación de imágenes para desencadenar eventos para su máscara.</span><span class="sxs-lookup"><span data-stu-id="16940-122">One of the most powerful features of Windows Media Player skins is that you can use image mapping to trigger events for your skin.</span></span> <span data-ttu-id="16940-123">Los mapas de imágenes son archivos que contienen imágenes especiales.</span><span class="sxs-lookup"><span data-stu-id="16940-123">Image maps are files that contain special images.</span></span> <span data-ttu-id="16940-124">Sin embargo, las imágenes de un archivo de mapa de imágenes no están destinadas a ser vistas por el usuario, pero las usa Windows Media Player para realizar acciones cuando el usuario hace clic en la máscara.</span><span class="sxs-lookup"><span data-stu-id="16940-124">The images in an image map file, however, are not meant to be viewed by the user, but are used by Windows Media Player to take action when the user clicks on your skin.</span></span>

<span data-ttu-id="16940-125">Los distintos controles necesitan distintos tipos de mapas de imagen.</span><span class="sxs-lookup"><span data-stu-id="16940-125">Different controls need different kinds of image maps.</span></span> <span data-ttu-id="16940-126">Por ejemplo, si hace color de una parte de un mapa de imágenes un valor rojo específico y el usuario hace clic en el área correspondiente de la imagen principal, un botón activará un evento.</span><span class="sxs-lookup"><span data-stu-id="16940-126">For example, if you color part of an image map a specific red value, and the user clicks on the corresponding area of your primary image, a button will fire an event.</span></span> <span data-ttu-id="16940-127">El color se usa para definir qué eventos se desencadenan haciendo clic en un área determinada de la máscara.</span><span class="sxs-lookup"><span data-stu-id="16940-127">Color is used to define which events are triggered by clicking in a particular area of the skin.</span></span>

## <a name="alternate-images"></a><span data-ttu-id="16940-128">Imágenes alternativas</span><span class="sxs-lookup"><span data-stu-id="16940-128">Alternate Images</span></span>

<span data-ttu-id="16940-129">También puede configurar imágenes alternativas para que se muestren cuando un usuario realiza alguna acción.</span><span class="sxs-lookup"><span data-stu-id="16940-129">You can also set up alternate images to display when a user does something.</span></span> <span data-ttu-id="16940-130">Por ejemplo, puede crear una imagen alternativa de un botón que se mostrará solo cuando se mantenga el mouse sobre el botón.</span><span class="sxs-lookup"><span data-stu-id="16940-130">For example, you can create an alternate image of a button that will be displayed only when the mouse hovers over the button.</span></span> <span data-ttu-id="16940-131">Esta es una buena manera de permitir que los usuarios sepan lo que pueden hacer y también permite una interfaz de usuario muy reconocible.</span><span class="sxs-lookup"><span data-stu-id="16940-131">This is a good way to let users know what they can do, and also allows for a highly discoverable user interface.</span></span> <span data-ttu-id="16940-132">Mediante el uso de la información sobre herramientas y las imágenes de desplazamiento detenidamente, puede crear interfaces de usuario inusuales que aún proporcionan los comentarios de los usuarios sobre las opciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="16940-132">By using ToolTips and hover images carefully, you can create unusual user interfaces that still give the user feedback about what options are available.</span></span>

<span data-ttu-id="16940-133">En las secciones siguientes se proporciona más información acerca de los archivos de imagen:</span><span class="sxs-lookup"><span data-stu-id="16940-133">The following sections provide more information about art files:</span></span>

-   [<span data-ttu-id="16940-134">Imágenes principales</span><span class="sxs-lookup"><span data-stu-id="16940-134">Primary Images</span></span>](primary-images.md)
-   [<span data-ttu-id="16940-135">Asignar imágenes</span><span class="sxs-lookup"><span data-stu-id="16940-135">Mapping Images</span></span>](mapping-images.md)
-   [<span data-ttu-id="16940-136">Imágenes alternativas</span><span class="sxs-lookup"><span data-stu-id="16940-136">Alternate Images</span></span>](alternate-images.md)
-   [<span data-ttu-id="16940-137">Formatos de archivo de imagen</span><span class="sxs-lookup"><span data-stu-id="16940-137">Art File Formats</span></span>](art-file-formats.md)
-   [<span data-ttu-id="16940-138">Ejemplo de arte sencillo</span><span class="sxs-lookup"><span data-stu-id="16940-138">Simple Art Example</span></span>](simple-art-example.md)

## <a name="related-topics"></a><span data-ttu-id="16940-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16940-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16940-140">**Archivos de máscara**</span><span class="sxs-lookup"><span data-stu-id="16940-140">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




