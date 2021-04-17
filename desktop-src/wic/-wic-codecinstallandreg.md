---
description: Al instalar un códec, debe registrarlo en el registro. También debe asegurarse de que la memoria caché de miniaturas se actualiza en caso de que ya existan imágenes en el formato en el equipo.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Instalación y registro de códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83616071bebdbab14bfdc7dd0f879df3d49789d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706483"
---
# <a name="codec-installation-and-registration"></a><span data-ttu-id="cc3e5-104">Instalación y registro de códecs</span><span class="sxs-lookup"><span data-stu-id="cc3e5-104">Codec Installation and Registration</span></span>

<span data-ttu-id="cc3e5-105">Al instalar un códec, debe registrarlo en el registro.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-105">When you install a codec, you must register it in the registry.</span></span> <span data-ttu-id="cc3e5-106">También debe asegurarse de que la memoria caché de miniaturas se actualiza en caso de que ya existan imágenes en el formato en el equipo.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-106">You must also make sure the thumbnail cache gets updated in case any images in your format already exist on the computer.</span></span>

<span data-ttu-id="cc3e5-107">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="cc3e5-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="cc3e5-108">Registro de un códec</span><span class="sxs-lookup"><span data-stu-id="cc3e5-108">Registering a Codec</span></span>](#registering-a-codec)
-   [<span data-ttu-id="cc3e5-109">Actualización de la caché en miniatura al instalar el códec</span><span class="sxs-lookup"><span data-stu-id="cc3e5-109">Updating the Thumbnail Cache When Installing Your Codec</span></span>](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [<span data-ttu-id="cc3e5-110">Poner el códec de WIC-Enabled a disposición de los usuarios</span><span class="sxs-lookup"><span data-stu-id="cc3e5-110">Making Your WIC-Enabled Codec Available To Users</span></span>](#making-your-wic-enabled-codec-available-to-users)
-   [<span data-ttu-id="cc3e5-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc3e5-111">Related topics</span></span>](#related-topics)

## <a name="registering-a-codec"></a><span data-ttu-id="cc3e5-112">Registro de un códec</span><span class="sxs-lookup"><span data-stu-id="cc3e5-112">Registering a Codec</span></span>

<span data-ttu-id="cc3e5-113">Al registrar un códec, en realidad está registrando dos componentes: el codificador y el descodificador.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-113">When you register a codec, you are actually registering two components: the encoder and the decoder.</span></span> <span data-ttu-id="cc3e5-114">También debe crear entradas del registro para registrar el formato de contenedor con los controladores de metadatos para los formatos de metadatos que admite el formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-114">You also need to make registry entries to register your container format with the metadata handlers for the metadata formats that your image format supports.</span></span>

<span data-ttu-id="cc3e5-115">En los temas siguientes se describen las entradas del registro necesarias para registrar el códec:</span><span class="sxs-lookup"><span data-stu-id="cc3e5-115">The following topics describe the registry entries you need to register your codec:</span></span>

[<span data-ttu-id="cc3e5-116">Entradas generales del registro</span><span class="sxs-lookup"><span data-stu-id="cc3e5-116">General Registry Entries</span></span>](-wic-generalregentries.md)

[<span data-ttu-id="cc3e5-117">Entradas del registro específicas del codificador</span><span class="sxs-lookup"><span data-stu-id="cc3e5-117">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)

[<span data-ttu-id="cc3e5-118">Entradas del registro específicas del descodificador</span><span class="sxs-lookup"><span data-stu-id="cc3e5-118">Decoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)

[<span data-ttu-id="cc3e5-119">Integración con la Galería fotográfica de Windows y el explorador de Windows</span><span class="sxs-lookup"><span data-stu-id="cc3e5-119">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a><span data-ttu-id="cc3e5-120">Actualización de la caché en miniatura al instalar el códec</span><span class="sxs-lookup"><span data-stu-id="cc3e5-120">Updating the Thumbnail Cache When Installing Your Codec</span></span>

<span data-ttu-id="cc3e5-121">Cuando se instala un códec, el instalador debe llamar a la función siguiente después de escribir sus entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-121">When a codec is installed, the installer needs to call the following function after writing its registry entries.</span></span>


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



<span data-ttu-id="cc3e5-122">Esta llamada notifica a Windows que la nueva información de Asociación de archivos está disponible.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-122">This call notifies Windows that new file association information is available.</span></span> <span data-ttu-id="cc3e5-123">Si ya existen imágenes en el formato de imagen en el equipo, la caché en miniatura contendrá miniaturas predeterminadas, ya que no hay ningún descodificador disponible para extraer las miniaturas cuando se adquirieron por primera vez.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-123">If images in your image format already exist on the computer, the thumbnail cache will contain default thumbnails for them because no decoder was available to extract the thumbnails when the images were first acquired.</span></span> <span data-ttu-id="cc3e5-124">Al notificar a Windows que hay disponible una nueva asociación de archivos, la caché en miniatura descarta cualquier miniatura vacía y extrae las miniaturas reales de los archivos que ahora se pueden descodificar.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-124">When you notify Windows that a new file association is available, the thumbnail cache discards any empty thumbnails and extracts the actual thumbnails from the files that can now be decoded.</span></span>

## <a name="making-your-wic-enabled-codec-available-to-users"></a><span data-ttu-id="cc3e5-125">Poner el códec de WIC-Enabled a disposición de los usuarios</span><span class="sxs-lookup"><span data-stu-id="cc3e5-125">Making Your WIC-Enabled Codec Available To Users</span></span>

<span data-ttu-id="cc3e5-126">Si es un fabricante de la cámara, puede enviar sus códecs sin formato en el cuadro con las cámaras.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-126">If you are a camera manufacturer, you can ship your raw codecs in the box with your cameras.</span></span> <span data-ttu-id="cc3e5-127">También puede publicar los códecs en la página de descarga del sitio Web.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-127">You can also post your codecs on the Download page of your Web site.</span></span> <span data-ttu-id="cc3e5-128">Sin embargo, si un usuario adquiere un archivo de imagen en el formato de otro origen, como un amigo, un socio comercial o algún otro sitio web, es posible que no sepa dónde obtener el códec para descodificarlo.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-128">However, if a user acquires an image file in your format from some other source, such as a friend, business associate, or some other Web site, they may not know where to get the codec to decode it with.</span></span>

<span data-ttu-id="cc3e5-129">Debido a este problema, Windows ofrece una forma más fácil de que los usuarios del formato de imagen encuentren el códec y lo descarguen en su equipo, a partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-129">Because of this issue, Windows offers an easier way for users of your image format to find your codec and download it onto their computer, starting with Windows Vista.</span></span> <span data-ttu-id="cc3e5-130">Si la Galería fotográfica de Windows reconoce una extensión de nombre de archivo como formato de imagen y el códec para ese formato no está instalado, un cuadro de diálogo indica al usuario que no se puede mostrar la foto y pregunta si el usuario desea descargar el software necesario para mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-130">If the Windows Photo Gallery recognizes a file name extension as an image format, and the codec for that format is not installed, a dialog box tells the user that the photo can’t be displayed, and asks whether the user wants to download the software required to display it.</span></span> <span data-ttu-id="cc3e5-131">Cuando el usuario acepta, aparece un sitio web hospedado por Microsoft con un vínculo al sitio de descarga del fabricante del códec.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-131">When the user accepts, a Microsoft-hosted Web site appears with a link to the codec manufacturer’s download site.</span></span> <span data-ttu-id="cc3e5-132">(Opcionalmente, puede solicitar que los usuarios se tomen directamente en el sitio de descarga).</span><span class="sxs-lookup"><span data-stu-id="cc3e5-132">(Optionally, you can request that users be taken directly to your download site.)</span></span>

<span data-ttu-id="cc3e5-133">Si desea que la Galería fotográfica de Windows reconozca las extensiones de nombre de archivo del formato de imagen para que los usuarios puedan dirigirse al sitio de descarga, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc3e5-133">If you want your image format’s file name extensions to be recognized by the Windows Photo Gallery so that users can be directed to your download site, you must do the following:</span></span>

1.  <span data-ttu-id="cc3e5-134">Proporcione un sitio de descarga para el códec.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-134">Provide a download site for your codec.</span></span> <span data-ttu-id="cc3e5-135">(Puede tener una página independiente para cada códec que proporcione o una página que proporcione descargas para todos los códecs).</span><span class="sxs-lookup"><span data-stu-id="cc3e5-135">(You can have a separate page for each codec you provide, or one page that provides downloads for all your codecs.)</span></span>

    <span data-ttu-id="cc3e5-136">El sitio de descarga debe localizarse y buscarse fácilmente en el modelo de cámara.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-136">The download site should be localized and easily searchable by camera model.</span></span>

2.  <span data-ttu-id="cc3e5-137">Proporcione a Microsoft una lista de extensiones para los formatos de imagen y las direcciones URL de los sitios de descarga.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-137">Provide Microsoft with a list of extensions for your image formats, and the URLs for your download sites.</span></span>

<span data-ttu-id="cc3e5-138">Debe informar a Microsoft de las extensiones de los nuevos códecs que desarrolle en el futuro y de cualquier cambio en las direcciones URL de los sitios de descarga, de modo que la nueva información se pueda agregar a la Galería fotográfica de Windows.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-138">You must inform Microsoft of the extensions for any new codecs you develop in the future, and of any changes to the URLs of your download sites, so that the new information can be added to the Windows Photo Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc3e5-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc3e5-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="cc3e5-140">**Vista**</span><span class="sxs-lookup"><span data-stu-id="cc3e5-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cc3e5-141">Implementación de IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="cc3e5-141">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="cc3e5-142">Conclusión (cómo escribir un códec WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="cc3e5-142">Conclusion (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[<span data-ttu-id="cc3e5-143">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="cc3e5-143">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="cc3e5-144">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="cc3e5-144">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



