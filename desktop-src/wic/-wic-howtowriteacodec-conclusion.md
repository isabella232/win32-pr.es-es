---
description: La compilación del códec en la plataforma de Windows Imaging Component (WIC) permite a todas las aplicaciones compiladas en WIC obtener la misma compatibilidad de plataforma para el formato de imagen que obtienen para los formatos de imagen comunes que se incluyen con la plataforma.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Conclusión (cómo escribir un códec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de165f20ff81094c3b64d7e9667795f0bf80cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720554"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="0c77f-103">Conclusión (cómo escribir un códec WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="0c77f-103">Conclusion (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="0c77f-104">La compilación del códec en la plataforma de Windows Imaging Component (WIC) permite a todas las aplicaciones compiladas en WIC obtener la misma compatibilidad de plataforma para el formato de imagen que obtienen para los formatos de imagen comunes que se incluyen con la plataforma.</span><span class="sxs-lookup"><span data-stu-id="0c77f-104">Building your codec on the Windows Imaging Component (WIC) platform makes it possible for all applications built on WIC to get the same platform support for your image format that they get for the common image formats shipped with the platform.</span></span> <span data-ttu-id="0c77f-105">También permite que la Galería fotográfica de Windows Vista, el explorador de Windows y el visor fotográfico muestren miniaturas y vistas previas de imágenes en el formato mediante el descodificador que proporcione.</span><span class="sxs-lookup"><span data-stu-id="0c77f-105">It also enables the Windows Vista Photo Gallery, Windows Explorer, and Photo Viewer to display thumbnails and previews of images in your format using the decoder that you provide.</span></span> <span data-ttu-id="0c77f-106">En el caso de los formatos sin procesar, permite que las aplicaciones de imágenes más sofisticadas aprovechen las capacidades de procesamiento sin procesar del descodificador.</span><span class="sxs-lookup"><span data-stu-id="0c77f-106">For raw formats, it enables more sophisticated imaging applications to take advantage of your decoder’s raw processing capabilities.</span></span> <span data-ttu-id="0c77f-107">En función de las opciones del codificador que admita, también puede exponer capacidades exclusivas del codificador para permitir que las aplicaciones saquen el máximo partido de las características avanzadas del formato de imagen.</span><span class="sxs-lookup"><span data-stu-id="0c77f-107">Depending on the encoder options you support, you can also expose unique capabilities of your encoder to enable applications to take full advantage of the advanced features of your image format.</span></span>

<span data-ttu-id="0c77f-108">El desarrollo de un códec habilitado para WIC requiere la implementación de algunas interfaces nuevas.</span><span class="sxs-lookup"><span data-stu-id="0c77f-108">Developing a WIC-enabled codec requires you to implement some new interfaces.</span></span> <span data-ttu-id="0c77f-109">En muchos casos, puede escribir un contenedor para el códec existente que implementa estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="0c77f-109">In many cases, you can write a wrapper for your existing codec that implements these interfaces.</span></span> <span data-ttu-id="0c77f-110">Al instalar el códec, debe realizar algunas entradas del registro para que la plataforma WIC pueda detectar el códec y asociarlo con los controladores de metadatos adecuados.</span><span class="sxs-lookup"><span data-stu-id="0c77f-110">When you install your codec, you must make some registry entries to make your codec discoverable by the WIC platform and associate it with the appropriate metadata handlers.</span></span> <span data-ttu-id="0c77f-111">También debe invocar una API para borrar la memoria caché en miniatura de las miniaturas predeterminadas (vacías) que puedan haber asociado previamente a las imágenes en el formato.</span><span class="sxs-lookup"><span data-stu-id="0c77f-111">You also need to invoke an API to clear the thumbnail cache of any default (empty) thumbnails that may have previously associated with images in your format.</span></span> <span data-ttu-id="0c77f-112">Si lo desea, puede habilitar la Galería fotográfica de Windows Vista para proporcionar a los usuarios un vínculo para descargar el códec cuando la Galería fotográfica encuentre una imagen con la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="0c77f-112">If you want, you can enable the Windows Vista Photo Gallery to provide users with a link to download your codec when the Photo Gallery encounters an image with your file name extension.</span></span> <span data-ttu-id="0c77f-113">Para ello, debe proporcionar a Microsoft información sobre la extensión de nombre de archivo del códec y la dirección URL del sitio de descarga.</span><span class="sxs-lookup"><span data-stu-id="0c77f-113">To do this, you must provide Microsoft with information about your codec’s file name extension and the URL for your download site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c77f-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0c77f-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0c77f-115">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0c77f-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0c77f-116">Instalación y registro de CÓDECs</span><span class="sxs-lookup"><span data-stu-id="0c77f-116">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="0c77f-117">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="0c77f-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="0c77f-118">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="0c77f-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



