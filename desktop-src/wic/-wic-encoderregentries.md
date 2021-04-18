---
description: Encoder-Specific entradas del registro
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific entradas del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e6fbfafa1f8d3b340d7e3864fddacb8cd7e282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720600"
---
# <a name="encoder-specific-registry-entries"></a><span data-ttu-id="dd714-103">Encoder-Specific entradas del registro</span><span class="sxs-lookup"><span data-stu-id="dd714-103">Encoder-Specific Registry Entries</span></span>


<span data-ttu-id="dd714-104">Además de las entradas indicadas anteriormente para el codificador, también debe registrar el codificador en la categoría de codificadores de componentes de imágenes de Windows (WIC) para que el motor de detección pueda encontrarlo.</span><span class="sxs-lookup"><span data-stu-id="dd714-104">In addition to the entries listed above for encoder, you must also register your encoder under the category of Windows Imaging Component (WIC) encoders so the discovery engine can find it.</span></span> <span data-ttu-id="dd714-105">Para ello, realice las siguientes entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="dd714-105">You do this by making the following registry entries.</span></span> <span data-ttu-id="dd714-106">El primer GUID en las siguientes entradas es el identificador de categoría (CATId) para WICBitmapEncoders.</span><span class="sxs-lookup"><span data-stu-id="dd714-106">The first GUID in the following entries is the category identifier (CATID) for WICBitmapEncoders.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a><span data-ttu-id="dd714-107">Registrar un formato de contenedor con escritores de metadatos</span><span class="sxs-lookup"><span data-stu-id="dd714-107">Registering a Container Format with Metadata Writers</span></span>

<span data-ttu-id="dd714-108">Si crea un nuevo formato de contenedor para el códec, también debe crear entradas del registro para admitir escritores de metadatos para los bloques de metadatos de las imágenes.</span><span class="sxs-lookup"><span data-stu-id="dd714-108">If you create a new container format for your codec, you must also create registry entries to support metadata writers for the metadata blocks in your images.</span></span> <span data-ttu-id="dd714-109">Las siguientes entradas deben crearse en el identificador de clase (CLSID) del escritor de metadatos para cada formato de metadatos admitido en el formato del contenedor.</span><span class="sxs-lookup"><span data-stu-id="dd714-109">The following entries need to be created under the class identifier (CLSID) of the metadata writer for each metadata format supported in your container format.</span></span> <span data-ttu-id="dd714-110">Si el códec usa un contenedor de Tagged Image File Format (TIFF), esta información ya está en el registro y no es necesario crear estas entradas.</span><span class="sxs-lookup"><span data-stu-id="dd714-110">If your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry and you don't need to create these entries.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Writer CLSID}
         Containers
            {Container Format GUID}
               WritePosition = Offset relative to its container
               WriteHeader = Pattern used for metadata header
               WriteOffset = Offset from beginning of header
```

<span data-ttu-id="dd714-111">Si usa un formato de contenedor de estilo TIFF o JPEG, debe registrar una asociación entre el contenedor y el formato del contenedor.</span><span class="sxs-lookup"><span data-stu-id="dd714-111">If you use a TIFF-style or JPEG-style container format, you must register an association between your container and that container format.</span></span> <span data-ttu-id="dd714-112">Para obtener más información, consulte la introducción [a la integración con la Galería fotográfica de Windows y el explorador de Windows](-wic-integrationregentries.md).</span><span class="sxs-lookup"><span data-stu-id="dd714-112">For more information, see the introduction in [Integration with Windows Photo Gallery and Windows Explorer](-wic-integrationregentries.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd714-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dd714-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dd714-114">**Vista**</span><span class="sxs-lookup"><span data-stu-id="dd714-114">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dd714-115">Entradas generales del registro</span><span class="sxs-lookup"><span data-stu-id="dd714-115">General Registry Entries</span></span>](-wic-generalregentries.md)
</dt> <dt>

[<span data-ttu-id="dd714-116">Entradas del registro específicas del codificador</span><span class="sxs-lookup"><span data-stu-id="dd714-116">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="dd714-117">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="dd714-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="dd714-118">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="dd714-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



