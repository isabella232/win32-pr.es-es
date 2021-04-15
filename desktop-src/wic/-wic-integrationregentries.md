---
description: Este tema se aplica a Windows Vista y versiones posteriores.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: Integración con la Galería fotográfica de Windows y el explorador de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ab2bb725b151a069f53a94a8fb2e31766132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648507"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a><span data-ttu-id="453ac-103">Integración con la Galería fotográfica de Windows y el explorador de Windows</span><span class="sxs-lookup"><span data-stu-id="453ac-103">Integration with Windows Photo Gallery and Windows Explorer</span></span>

<span data-ttu-id="453ac-104">Este tema se aplica a Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="453ac-104">This topic applies to Windows Vista and later.</span></span> <span data-ttu-id="453ac-105">Contiene las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="453ac-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="453ac-106">Introducción</span><span class="sxs-lookup"><span data-stu-id="453ac-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="453ac-107">Integración con el almacén de propiedades de Windows</span><span class="sxs-lookup"><span data-stu-id="453ac-107">Integration with the Windows Property Store</span></span>](#integration-with-the-windows-property-store)
-   [<span data-ttu-id="453ac-108">Integración con la Galería fotográfica de Windows</span><span class="sxs-lookup"><span data-stu-id="453ac-108">Integration with the Windows Photo Gallery</span></span>](#integration-with-the-windows-photo-gallery)
-   [<span data-ttu-id="453ac-109">Integración con la caché en miniatura de Windows</span><span class="sxs-lookup"><span data-stu-id="453ac-109">Integration with the Windows Thumbnail Cache</span></span>](#integration-with-the-windows-thumbnail-cache)
-   [<span data-ttu-id="453ac-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="453ac-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="453ac-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="453ac-111">Introduction</span></span>

<span data-ttu-id="453ac-112">Para habilitar la Galería fotográfica de Windows y el explorador de Windows para Mostrar miniaturas y buscar y actualizar los metadatos de imagen estándar, un códec debe tener una implementación de las interfaces [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) y [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) asociadas a él.</span><span class="sxs-lookup"><span data-stu-id="453ac-112">To enable Windows Photo Gallery and Windows Explorer to display thumbnails and search and update standard image metadata, a codec must have an implementation of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) and [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces associated with it.</span></span> <span data-ttu-id="453ac-113">La interfaz IThumbnailProvider se usa para recuperar miniaturas y rellenar la caché en miniatura, y la interfaz IPropertyStore se usa para buscar y actualizar los metadatos asociados a un archivo.</span><span class="sxs-lookup"><span data-stu-id="453ac-113">The IThumbnailProvider interface is used to retrieve thumbnails and populate the thumbnail cache, and the IPropertyStore interface is used for searching and updating metadata associated with a file.</span></span> <span data-ttu-id="453ac-114">A partir de Windows Vista, todos los tipos de archivo tienen vistas en miniatura y metadatos, pero los distintos tipos de archivo requieren implementaciones diferentes de estas interfaces para recuperar o generar las miniaturas y metadatos para ellos.</span><span class="sxs-lookup"><span data-stu-id="453ac-114">As of Windows Vista, all file types have thumbnails and metadata, but different file types require different implementations of these interfaces to retrieve or generate the thumbnails and metadata for them.</span></span> <span data-ttu-id="453ac-115">El sistema proporciona implementaciones predeterminadas de estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="453ac-115">The system provides default implementations of these interfaces.</span></span> <span data-ttu-id="453ac-116">La implementación predeterminada de IThumbnailProvider se puede usar para cualquier formato de imagen habilitado para Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="453ac-116">The default implementation of IThumbnailProvider can be used for any Windows Imaging Component (WIC)–enabled image format.</span></span> <span data-ttu-id="453ac-117">La implementación predeterminada de IPropertyStore se puede usar con cualquier formato de imagen habilitado para WIC que esté basado en un contenedor Tagged Image File Format (TIFF) o JPEG.</span><span class="sxs-lookup"><span data-stu-id="453ac-117">The default implementation of IPropertyStore can be used with any WIC-enabled image format that is based on a Tagged Image File Format (TIFF) or JPEG container.</span></span> <span data-ttu-id="453ac-118">Para asociar el formato de imagen con las implementaciones predeterminadas de estas dos interfaces, debe agregar solo algunas entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="453ac-118">To associate your image format with the default implementations of both of these interfaces, you must add just a few registry entries.</span></span>

<span data-ttu-id="453ac-119">Las siguientes entradas indican a la Galería fotográfica de Windows y al explorador de Windows que una extensión de nombre de archivo (. ext) y su tipo MIME asociado están asociados a un formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="453ac-119">The following entries indicate to the Windows Photo Gallery and Windows Explorer that a file name extension (.ext) and its associated MIME type are associated with an image format.</span></span>

<span data-ttu-id="453ac-120">La entrada siguiente indica a Windows y a las aplicaciones que usan el tipo de contenido (también conocido como tipo MIME) que un archivo con una extensión determinada (. ext) es un formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="453ac-120">The following entry indicates to Windows and applications that use content type (also known as mime type) that a file with a given extension (.ext) is an image format.</span></span> <span data-ttu-id="453ac-121">El propietario del tipo de archivo debe elegir un `<image sub type value>` que identifique de forma única el formato de archivo y este valor de tipo de contenido debe registrarse con IANA.</span><span class="sxs-lookup"><span data-stu-id="453ac-121">The file type owner needs to choose a `<image sub type value>` that uniquely identifies the file format and this content type value needs to be register with IANA.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

<span data-ttu-id="453ac-122">La entrada siguiente indica a Windows, a Windows Search y a las aplicaciones que usan [System. Kind](../properties/props-system-kind.md) que una extensión de nombre de archivo (. ext) debe tratarse como una imagen.</span><span class="sxs-lookup"><span data-stu-id="453ac-122">The following entry indicates to Windows, Windows search and applications that use [System.Kind](../properties/props-system-kind.md) that a file name extension (.ext) should be treated as a picture.</span></span> <span data-ttu-id="453ac-123">En concreto, indica que la propiedad System. Kind de la extensión de archivo debe establecerse en Picture.</span><span class="sxs-lookup"><span data-stu-id="453ac-123">Specifically, it indicates that the file extension’s System.Kind property should be set to Picture.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     {.ext} = Picture
```

## <a name="integration-with-the-windows-property-store"></a><span data-ttu-id="453ac-124">Integración con el almacén de propiedades de Windows</span><span class="sxs-lookup"><span data-stu-id="453ac-124">Integration with the Windows Property Store</span></span>

<span data-ttu-id="453ac-125">A veces, las mismas propiedades de metadatos se exponen en distintos esquemas de metadatos, a menudo con distintos nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="453ac-125">Sometimes the same metadata properties are exposed in different metadata schemas, often with different property names.</span></span> <span data-ttu-id="453ac-126">Cuando se actualiza una de estas propiedades, pero no las demás, los metadatos del archivo pueden no estar sincronizados. El controlador de propiedades de fotografía proporciona la implementación predeterminada de **IPropertyStore** para las imágenes y la usan las aplicaciones, así como la Galería fotográfica de Windows y el explorador de Windows para asegurarse de que todos los metadatos de una imagen permanecen sincronizados y que las propiedades mostradas por las aplicaciones son coherentes con las que se muestran en la Galería fotográfica de Windows y el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="453ac-126">When one of these properties is updated, but the others are not, the metadata within the file can get out of sync. The photo property handler provides the default **IPropertyStore** implementation for images, and is used by applications as well as by the Windows Photo Gallery and Windows Explorer to ensure that all the metadata in an image stays in sync, and that the properties displayed by applications are consistent with those displayed by the Windows Photo Gallery and Windows Explorer.</span></span> <span data-ttu-id="453ac-127">Cuando el controlador de propiedades de la fotografía actualiza los metadatos, se asegura de que estas propiedades se actualizan de forma coherente en todos los formatos de metadatos comunes que se encuentran en el archivo.</span><span class="sxs-lookup"><span data-stu-id="453ac-127">When the photo property handler updates metadata, it makes sure that these properties are updated consistently across all the common metadata formats that are present in the file.</span></span>

<span data-ttu-id="453ac-128">El controlador de la propiedad Photo debe comprender el formato del contenedor y cómo buscar las distintas propiedades que contiene.</span><span class="sxs-lookup"><span data-stu-id="453ac-128">The photo property handler must understand the container format and how to locate the various properties within it.</span></span> <span data-ttu-id="453ac-129">En general, no es posible que el controlador de la propiedad Photo sepa cómo se colocan los distintos bloques de metadatos en un formato de contenedor propietario.</span><span class="sxs-lookup"><span data-stu-id="453ac-129">In general, it isn’t possible for the photo property handler to know how the various metadata blocks are laid out in a proprietary container format.</span></span> <span data-ttu-id="453ac-130">Sin embargo, si los metadatos del formato de contenedor se disponen de la misma manera que los metadatos en un formato de contenedor TIFF o en un formato de contenedor JPEG, el controlador de propiedades de fotografía puede aprovechar este conocimiento para actualizar los metadatos de forma coherente también en el formato de contenedor.</span><span class="sxs-lookup"><span data-stu-id="453ac-130">However, if the metadata in your container format is laid out the same way as the metadata in either a TIFF container format or a JPEG container format, the photo property handler can take advantage of that knowledge to update metadata consistently in your container format as well.</span></span>

<span data-ttu-id="453ac-131">Puede registrar esta asociación creando la siguiente entrada del registro.</span><span class="sxs-lookup"><span data-stu-id="453ac-131">You can register this association by creating the following registry entry.</span></span> <span data-ttu-id="453ac-132">Esta entrada notifica al controlador de propiedades de la fotografía que el formato de contenedor identificado por este GUID entiende las mismas rutas de acceso de lenguaje de consulta de metadatos que el formato de contenedor con el GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3.</span><span class="sxs-lookup"><span data-stu-id="453ac-132">This entry notifies the photo property handler that the container format identified by this GUID understands the same metadata query language paths as the container format with the GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3.</span></span> <span data-ttu-id="453ac-133">(163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 es el GUID para el formato de contenedor TIFF).</span><span class="sxs-lookup"><span data-stu-id="453ac-133">(163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 is the GUID for the TIFF container format.)</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  ContainerAssociations
                     {Container Format GUID} = {163bcc30-e2e9-4f0b-961d-a3e9fdb788a3}
```

<span data-ttu-id="453ac-134">La entrada siguiente asocia la implementación predeterminada del controlador de la propiedad de foto de **IPropertyStore** con los archivos que tienen la extensión ". ext".</span><span class="sxs-lookup"><span data-stu-id="453ac-134">The following entry associates the photo property handler’s default implementation of **IPropertyStore** with files that have the extension ".ext".</span></span> <span data-ttu-id="453ac-135">El primer GUID es el IID de la interfaz **IPropertyStore** y el segundo es el GUID de la implementación del controlador de propiedades de la fotografía.</span><span class="sxs-lookup"><span data-stu-id="453ac-135">The first GUID is the IID of the **IPropertyStore** interface, and the second is the GUID of the photo property handler’s implementation of it.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  {.ext}
                     (Default) = {a38b883c-1682-497e-97b0-0a3a9e801682}
```

<span data-ttu-id="453ac-136">Los códecs que usan un formato propietario que no es compatible con el formato de contenedor TIFF o JPEG deben escribir su propia implementación de **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="453ac-136">Codecs that use a proprietary format that is not compatible with either the TIFF or JPEG container format must write their own **IPropertyStore** implementation.</span></span>

## <a name="integration-with-the-windows-photo-gallery"></a><span data-ttu-id="453ac-137">Integración con la Galería fotográfica de Windows</span><span class="sxs-lookup"><span data-stu-id="453ac-137">Integration with the Windows Photo Gallery</span></span>

<span data-ttu-id="453ac-138">La Galería fotográfica de Windows se basa en WIC y puede mostrar cualquier formato de imagen habilitado para WIC para el que esté instalado el códec.</span><span class="sxs-lookup"><span data-stu-id="453ac-138">Windows Photo Gallery is built on WIC and can display any WIC-enabled image format for which the codec is installed.</span></span> <span data-ttu-id="453ac-139">Para notificar al sistema que el formato de imagen se puede abrir en la Galería fotográfica de Windows, debe crear una asociación de archivo creando las siguientes entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="453ac-139">To notify the system that your image format can be opened in Windows Photo Gallery, you need to create a file association by creating the following registry entries.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      (Default) = {ProgID} for example, jpegfile)
      OpenWithProgids
         {ProgID}
      OpenWithList
         PhotoViewer.dll
      ShellEx
         ContextMenuHandlers
            ShellImagePreview
               (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   SystemFileAssociations
      {.ext}
         OpenWithList
            PhotoViewer.dll
         ShellEx
            ContextMenuHandlers
               ShellImagePreview
                  (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   {Image Format ProgID}
      (Default) = Name of Image Format
      DefaultIcon
         (Default) = Path to icon for type, icon index
      shell
         open
            MuiVerb = @%PROGRAMFILES%\Windows Photo Gallery\photoviewer.dll,-3043
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%ProgramFiles%\Windows Photo Gallery\PhotoViewer.dll", ImageView_Fullscreen %1
            DropTarget
               Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
         printo
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%SystemRoot%\System32\shimgvw.dll", ImageView_PrintTo /pt "%1" "%2" "%3" "%4"
```

<span data-ttu-id="453ac-140">El ProgID suele ser la extensión de nombre de archivo anexada con la palabra "File".</span><span class="sxs-lookup"><span data-stu-id="453ac-140">The ProgID is usually the file name extension appended with the word "file".</span></span> <span data-ttu-id="453ac-141">(Por ejemplo, si la extensión de nombre de archivo es. txt, el ProgID sería normalmente "TXTfile").</span><span class="sxs-lookup"><span data-stu-id="453ac-141">(For example, if the file name extension is .txt, the ProgID would usually be "txtfile".)</span></span>

<span data-ttu-id="453ac-142">Hay otras entradas de registro estándar que es posible que tenga que crear para admitir asociaciones de archivo. sin embargo, como los the'y no son específicos de WIC, quedan fuera del ámbito de este tema.</span><span class="sxs-lookup"><span data-stu-id="453ac-142">There are other standard registry entries you may need to create to support file associations; however, because the’y are not specific to WIC, they are beyond the scope of this topic.</span></span>

## <a name="integration-with-the-windows-thumbnail-cache"></a><span data-ttu-id="453ac-143">Integración con la caché en miniatura de Windows</span><span class="sxs-lookup"><span data-stu-id="453ac-143">Integration with the Windows Thumbnail Cache</span></span>

<span data-ttu-id="453ac-144">Las dos entradas siguientes indican que la implementación del proveedor de miniaturas de WIC estándar se puede usar para recuperar miniaturas de archivos con esta extensión.</span><span class="sxs-lookup"><span data-stu-id="453ac-144">The following two entries indicate that the standard WIC thumbnail provider implementation can be used to retrieve thumbnails for files with this extension.</span></span> <span data-ttu-id="453ac-145">El primer GUID es el IID de la interfaz [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) y el segundo es el GUID de la implementación estándar del sistema de esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="453ac-145">The first GUID is the IID of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) interface, and the second is the GUID of the standard system implementation of this interface.</span></span> <span data-ttu-id="453ac-146">(Todas las entradas de HLCR \\ . ext \\ ShellEx \\ se repiten en HKCR \\ SystemFileAssociations \\ . ext \\ ShellEx \\ ).</span><span class="sxs-lookup"><span data-stu-id="453ac-146">(All entries under HLCR\\.ext\\ShellEx\\ are repeated under HKCR\\SystemFileAssociations\\.ext\\ShellEx\\.)</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a><span data-ttu-id="453ac-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="453ac-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="453ac-148">**Vista**</span><span class="sxs-lookup"><span data-stu-id="453ac-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="453ac-149">Entradas del registro específicas del codificador</span><span class="sxs-lookup"><span data-stu-id="453ac-149">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="453ac-150">Instalación y registro de CÓDECs</span><span class="sxs-lookup"><span data-stu-id="453ac-150">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="453ac-151">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="453ac-151">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="453ac-152">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="453ac-152">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
