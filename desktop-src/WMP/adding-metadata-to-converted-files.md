---
title: Agregar metadatos a archivos convertidos
description: Agregar metadatos a archivos convertidos
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Windows Media Player, proceso de conversión
- Complementos de Windows Media Player, conversión
- complementos, conversión
- Complementos de conversión, agregar metadatos a archivos convertidos
- agregar metadatos a archivos convertidos
- metadatos, agregar a archivos convertidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4ae47318089149564f64832c95e4cee1b27f26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791950"
---
# <a name="adding-metadata-to-converted-files"></a><span data-ttu-id="9b5aa-109">Agregar metadatos a archivos convertidos</span><span class="sxs-lookup"><span data-stu-id="9b5aa-109">Adding Metadata to Converted Files</span></span>

<span data-ttu-id="9b5aa-110">Los archivos convertidos deben contener determinados metadatos para garantizar una buena experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="9b5aa-110">Converted files must contain certain metadata to ensure a good user experience.</span></span> <span data-ttu-id="9b5aa-111">Como mínimo, los archivos convertidos deben contener los atributos principales que aparecen en las instrucciones de uso de los [metadatos de Windows Media](/previous-versions/ms867702(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="9b5aa-111">At a minimum, converted files must contain the primary attributes listed in the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)).</span></span>

<span data-ttu-id="9b5aa-112">En el caso de los archivos de música, establezca el valor de **WM/MediaClassPrimaryID** en D1607DBC-E323-4BE2-86A1-48A42A28441E.</span><span class="sxs-lookup"><span data-stu-id="9b5aa-112">For music files, set the value for **WM/MediaClassPrimaryID** to D1607DBC-E323-4BE2-86A1-48A42A28441E.</span></span>

<span data-ttu-id="9b5aa-113">En el caso de los archivos de correo de voz, establezca el valor de **WM/MediaClassPrimaryID** en 01CD0F29-DA4E-4157-897B-6275D50C4F11, que es el GUID de clase principal para los archivos de audio.</span><span class="sxs-lookup"><span data-stu-id="9b5aa-113">For voicemail files, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11, which is the primary class GUID for audio files.</span></span> <span data-ttu-id="9b5aa-114">Establezca el valor de **WM/MediaClassSecondaryID** en 193c8824-4d52-4178-90bd-305240b04636.</span><span class="sxs-lookup"><span data-stu-id="9b5aa-114">Set the value for **WM/MediaClassSecondaryID** to 193c8824-4d52-4178-90bd-305240b04636.</span></span>

<span data-ttu-id="9b5aa-115">En el caso de las notas de voz, establezca el valor de **WM/MediaClassPrimaryID** en 01CD0F29-DA4E-4157-897B-6275D50C4F11.</span><span class="sxs-lookup"><span data-stu-id="9b5aa-115">For voice notes, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11.</span></span> <span data-ttu-id="9b5aa-116">Establezca el valor de **WM/MediaClassSecondaryID** en 3A172A13-2BD9-4831-835B-114F6A95943F.</span><span class="sxs-lookup"><span data-stu-id="9b5aa-116">Set the value for **WM/MediaClassSecondaryID** to 3A172A13-2BD9-4831-835B-114F6A95943F.</span></span>

<span data-ttu-id="9b5aa-117">Establezca el valor de **WM/ContentDistributor** en el nombre de clave del servicio de música que proporcionó el contenido.</span><span class="sxs-lookup"><span data-stu-id="9b5aa-117">Set the value for **WM/ContentDistributor** to the key name for the music service that provided the content.</span></span>

<span data-ttu-id="9b5aa-118">Establezca el valor de **WM/UniqueFileIdentifier** en el ID. de contenido.</span><span class="sxs-lookup"><span data-stu-id="9b5aa-118">Set the value for **WM/UniqueFileIdentifier** to the content ID.</span></span> <span data-ttu-id="9b5aa-119">Esto le permitirá recuperar elementos de contenido específicos en el futuro.</span><span class="sxs-lookup"><span data-stu-id="9b5aa-119">This will enable you to retrieve specific content items at a future time.</span></span>

<span data-ttu-id="9b5aa-120">Establezca un valor para **WM/WMShadowFileSourceFileType**.</span><span class="sxs-lookup"><span data-stu-id="9b5aa-120">Set a value for **WM/WMShadowFileSourceFileType**.</span></span>

<span data-ttu-id="9b5aa-121">Para contenido protegido, use el SDK de Windows Media Format para establecer el atributo **\_ DRMHeader \_ contentid de DRM** en el ID. de contenido.</span><span class="sxs-lookup"><span data-stu-id="9b5aa-121">For protected content, use the Windows Media Format SDK to set the **DRM\_DRMHeader\_ContentID** attribute to the content ID.</span></span>

<span data-ttu-id="9b5aa-122">Para contenido protegido, establezca un valor para **WM/WMShadowFileSourceDRMType**.</span><span class="sxs-lookup"><span data-stu-id="9b5aa-122">For protected content, set a value for **WM/WMShadowFileSourceDRMType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b5aa-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b5aa-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b5aa-124">**Acerca de los complementos de conversión**</span><span class="sxs-lookup"><span data-stu-id="9b5aa-124">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="9b5aa-125">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="9b5aa-125">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 