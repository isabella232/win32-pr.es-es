---
title: Compatibilidad con imágenes personalizadas para dispositivos
description: Compatibilidad con imágenes personalizadas para dispositivos
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Windows Media Player, compatibilidad con imágenes personalizadas para dispositivos
- Windows Media Player, compatibilidad con imágenes para dispositivos
- compatibilidad con imágenes personalizadas de dispositivo
- compatibilidad con imágenes personalizadas para dispositivos
- compatibilidad con imágenes para dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffdf318df39935e844cc84919bb4d6e50cc259a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695684"
---
# <a name="custom-image-support-for-devices"></a><span data-ttu-id="93a41-108">Compatibilidad con imágenes personalizadas para dispositivos</span><span class="sxs-lookup"><span data-stu-id="93a41-108">Custom Image Support for Devices</span></span>

> [!Note]  
> <span data-ttu-id="93a41-109">En esta sección se documenta una característica de Windows Media Player 10 que está disponible al usar el sistema operativo Windows XP.</span><span class="sxs-lookup"><span data-stu-id="93a41-109">This section documents a feature of Windows Media Player 10 that is available when using the Windows XP operating system.</span></span> <span data-ttu-id="93a41-110">Puede que no esté disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="93a41-110">It may be unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="93a41-111">Los fabricantes de dispositivos pueden proporcionar dos archivos de imagen especiales para personalizar el modo en que se representa un dispositivo en la interfaz de usuario de Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="93a41-111">Device manufacturers can provide two special image files to customize the way a device is represented in the Windows Media Player 10 user interface.</span></span> <span data-ttu-id="93a41-112">Estos dos archivos son:</span><span class="sxs-lookup"><span data-stu-id="93a41-112">These two files are:</span></span>

-   <span data-ttu-id="93a41-113">DevIcon. fil.</span><span class="sxs-lookup"><span data-stu-id="93a41-113">DevIcon.fil.</span></span> <span data-ttu-id="93a41-114">Un archivo de formato de icono de Windows que representa el hardware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93a41-114">A Windows icon format file that represents the device hardware.</span></span> <span data-ttu-id="93a41-115">Esta imagen se muestra en Windows Media Player 10 en cualquier lugar donde se use un icono para representar un dispositivo, como la lista de dispositivos en la característica de **sincronización** .</span><span class="sxs-lookup"><span data-stu-id="93a41-115">This image displays in Windows Media Player 10 anywhere an icon is used to represent a device, such as the device list in the **Sync** feature.</span></span>
-   <span data-ttu-id="93a41-116">DevLogo. fil.</span><span class="sxs-lookup"><span data-stu-id="93a41-116">DevLogo.fil.</span></span> <span data-ttu-id="93a41-117">Un archivo de formato PNG que representa el logotipo corporativo del fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93a41-117">A PNG format file that represents the corporate logo of the device manufacturer.</span></span> <span data-ttu-id="93a41-118">Esta imagen se muestra en Windows Media Player 10 Anywhere se usa la personalización de marca corporativa, como el cuadro de diálogo de **instalación del dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="93a41-118">This image displays in Windows Media Player 10 anywhere corporate branding is used, such as the **Device Setup** dialog box.</span></span>

## <a name="general-guidelines-for-images"></a><span data-ttu-id="93a41-119">Directrices generales para imágenes</span><span class="sxs-lookup"><span data-stu-id="93a41-119">General Guidelines for Images</span></span>

<span data-ttu-id="93a41-120">Las siguientes directrices se aplican a la compatibilidad con imágenes personalizadas en general:</span><span class="sxs-lookup"><span data-stu-id="93a41-120">The following guidelines apply to custom image support in general:</span></span>

-   <span data-ttu-id="93a41-121">Esta característica es opcional.</span><span class="sxs-lookup"><span data-stu-id="93a41-121">This feature is optional.</span></span> <span data-ttu-id="93a41-122">Los dispositivos que no suministran imágenes se representarán mediante imágenes predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="93a41-122">Devices that do not supply images will be represented by default images.</span></span>
-   <span data-ttu-id="93a41-123">Esta característica solo es compatible con dispositivos habilitados para MTP.</span><span class="sxs-lookup"><span data-stu-id="93a41-123">This feature is supported for MTP-enabled devices only.</span></span>
-   <span data-ttu-id="93a41-124">Para evitar cambios en los archivos, se recomienda que los archivos de imagen se almacenen en el firmware o en un medio de almacenamiento protegido, no en los archivos creados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="93a41-124">To prevent changes to the files, it is recommended that the image files be stored in firmware or a protected storage medium, not with user-created files.</span></span>
-   <span data-ttu-id="93a41-125">Los archivos no se deben devolver a Windows Media Administrador de dispositivos clientes que enumeran el almacenamiento raíz del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93a41-125">The files should not be returned to Windows Media Device Manager clients that enumerate the root storage of the device.</span></span> <span data-ttu-id="93a41-126">Además, se debe producir un error al eliminar, mover o cambiar el nombre de los archivos.</span><span class="sxs-lookup"><span data-stu-id="93a41-126">Also, deleting, moving, or renaming the files should fail.</span></span>
-   <span data-ttu-id="93a41-127">Si el dispositivo proporciona más de un medio de almacenamiento, el dispositivo debe devolver los archivos de imagen en respuesta a las solicitudes de apertura de archivos de cualquier medio.</span><span class="sxs-lookup"><span data-stu-id="93a41-127">If the device provides more than one storage medium, the device should return the image files in response to file open requests from any medium.</span></span> <span data-ttu-id="93a41-128">Se pueden devolver iconos de dispositivo diferentes de cada medio de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="93a41-128">Different device icons may be returned from each storage medium.</span></span>
-   <span data-ttu-id="93a41-129">En el caso de los clientes habilitados para Windows Media Administrador de dispositivos 1,2, estas imágenes tendrán prioridad sobre las propiedades de icono suministradas por los mecanismos de instalación de Windows, como las propiedades de nodo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93a41-129">For Windows Media Device Manager 1.2-enabled clients, these images will take precedence over icon properties supplied by Windows setup mechanisms, such as device node properties.</span></span>
-   <span data-ttu-id="93a41-130">Las imágenes no deben contener ninguna información que requiera localización.</span><span class="sxs-lookup"><span data-stu-id="93a41-130">The images must not contain any information that requires localization.</span></span>
-   <span data-ttu-id="93a41-131">En el caso de los dispositivos de varias funciones, solo las características de reproducción de música de Windows XP usarán estas imágenes.</span><span class="sxs-lookup"><span data-stu-id="93a41-131">For multi-function devices, only the music playback features of Windows XP will use these images.</span></span>

## <a name="creating-the-device-icon-image"></a><span data-ttu-id="93a41-132">Crear la imagen del icono del dispositivo</span><span class="sxs-lookup"><span data-stu-id="93a41-132">Creating the Device Icon Image</span></span>

<span data-ttu-id="93a41-133">El archivo de imagen del icono del dispositivo, DevIcon. fil, debe contener un archivo en formato de icono de Windows.</span><span class="sxs-lookup"><span data-stu-id="93a41-133">The device icon image file, DevIcon.fil, must contain a file in Windows icon format.</span></span> <span data-ttu-id="93a41-134">Los [iconos de los artículos de MSDN en Win32](/previous-versions/ms997538(v=msdn.10)) describen cómo crear este tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="93a41-134">The MSDN article [Icons in Win32](/previous-versions/ms997538(v=msdn.10)) describes how to create such a file.</span></span> <span data-ttu-id="93a41-135">En el artículo de MSDN [crear iconos de Windows XP](/previous-versions/ms997636(v=msdn.10)) se proporcionan instrucciones de estilo para los iconos de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="93a41-135">The MSDN article [Creating Windows XP Icons](/previous-versions/ms997636(v=msdn.10)) provides style guidelines for Windows XP icons.</span></span> <span data-ttu-id="93a41-136">El archivo de imagen del icono del dispositivo incorpora doce imágenes en un único archivo, ya que proporciona cuatro tamaños diferentes con tres profundidades de color diferentes cada una.</span><span class="sxs-lookup"><span data-stu-id="93a41-136">The device icon image file incorporates twelve images in a single file by providing four different sizes with three different color depths each.</span></span>

<span data-ttu-id="93a41-137">Asegúrese de prestar especial atención a las siguientes directrices:</span><span class="sxs-lookup"><span data-stu-id="93a41-137">Be certain to pay particular attention to the following guidelines:</span></span>

-   <span data-ttu-id="93a41-138">Los tamaños recomendados (en píxeles) son 16x16, 32x32, 48x48 y 256x256.</span><span class="sxs-lookup"><span data-stu-id="93a41-138">Recommended sizes (in pixels) are 16x16, 32x32, 48x48, and 256x256.</span></span>
-   <span data-ttu-id="93a41-139">Las profundidades de color recomendadas son de 24 bits con canal alfa de 8 bits, de 8 bits con transparencia de 1 bit y de 4 bits con transparencia de 1 bit.</span><span class="sxs-lookup"><span data-stu-id="93a41-139">Recommended color depths are 24-bit with 8-bit alpha channel, 8-bit with 1-bit transparency, and 4-bit with 1-bit transparency.</span></span>
-   <span data-ttu-id="93a41-140">Use las recomendaciones de ángulo de perspectiva y sombra paralela que se describen en los artículos de MSDN mencionados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="93a41-140">Use the perspective angle and drop shadow recommendations described in the MSDN articles mentioned previously.</span></span>

<span data-ttu-id="93a41-141">Una vez que haya creado el archivo de icono, simplemente cambie el nombre de DevIcon. fil.</span><span class="sxs-lookup"><span data-stu-id="93a41-141">Once you have created the icon file, simply rename it DevIcon.fil.</span></span>

## <a name="creating-the-corporate-logo-image"></a><span data-ttu-id="93a41-142">Creación de la imagen de logotipo corporativo</span><span class="sxs-lookup"><span data-stu-id="93a41-142">Creating the Corporate Logo Image</span></span>

<span data-ttu-id="93a41-143">El archivo de imagen del logotipo corporativo, DevLogo. fil, debe contener un archivo en formato PNG.</span><span class="sxs-lookup"><span data-stu-id="93a41-143">The corporate logo image file, DevLogo.fil, must contain a file in PNG format.</span></span> <span data-ttu-id="93a41-144">Siga estas instrucciones al crear la imagen:</span><span class="sxs-lookup"><span data-stu-id="93a41-144">Use the following guidelines when creating the image:</span></span>

-   <span data-ttu-id="93a41-145">Las dimensiones máximas de la imagen son 150x32 píxeles.</span><span class="sxs-lookup"><span data-stu-id="93a41-145">The maximum dimensions for the image are 150x32 pixels.</span></span>
-   <span data-ttu-id="93a41-146">La imagen debe admitir la combinación alfa para permitir una transición fluida entre la interfaz de usuario de Windows Media Player 10 y el logotipo.</span><span class="sxs-lookup"><span data-stu-id="93a41-146">The image should support alpha blending to enable a smooth transition between the Windows Media Player 10 user interface and the logo.</span></span>

<span data-ttu-id="93a41-147">Una vez que haya creado el archivo de logotipo corporativo, simplemente cambie el nombre de DevLogo. fil.</span><span class="sxs-lookup"><span data-stu-id="93a41-147">Once you have created the corporate logo file, simply rename it DevLogo.fil.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93a41-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93a41-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93a41-149">**Reproductor de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="93a41-149">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 