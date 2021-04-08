---
title: Compatibilidad con ID3
description: ID3 es una organización que ha definido un conjunto de estándares para incluir metadatos en archivos de audio MPEG Layer-3 (MP3).
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- SDK de Windows Media Format, compatibilidad con ID3
- Advanced Systems Format (ASF), compatibilidad con ID3
- ASF (formato de sistemas avanzados), compatibilidad con ID3
- metadatos, ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f356dae63b1d3672b584bb61956f478b67a697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778906"
---
# <a name="id3-support"></a><span data-ttu-id="a0fc8-108">Compatibilidad con ID3</span><span class="sxs-lookup"><span data-stu-id="a0fc8-108">ID3 Support</span></span>

<span data-ttu-id="a0fc8-109">ID3 es una organización que ha definido un conjunto de estándares para incluir metadatos en archivos de audio MPEG Layer-3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="a0fc8-109">ID3 is an organization that has defined a set of standards for including metadata in MPEG Layer-3 (MP3) audio files.</span></span> <span data-ttu-id="a0fc8-110">Los objetos del SDK de Windows Media Format proporcionan compatibilidad con atributos compatibles con ID3.</span><span class="sxs-lookup"><span data-stu-id="a0fc8-110">The objects of the Windows Media Format SDK provide support for ID3 compatible attributes.</span></span> <span data-ttu-id="a0fc8-111">Se admiten tres versiones diferentes de ID3: ID3v1. x, ID3v 2.2 y ID3v 2.3/V2, 4.</span><span class="sxs-lookup"><span data-stu-id="a0fc8-111">Three distinct ID3 versions are supported: ID3v1.x, ID3v2.2, and ID3v2.3/v2,4.</span></span> <span data-ttu-id="a0fc8-112">Para obtener una lista de los atributos que son equivalentes a los fotogramas ID3, consulte [compatibilidad con etiquetas ID3](id3-tag-support.md).</span><span class="sxs-lookup"><span data-stu-id="a0fc8-112">For a list of the attributes that equate to ID3 frames, see [ID3 Tag Support](id3-tag-support.md).</span></span>

<span data-ttu-id="a0fc8-113">A menos que se indique lo contrario, los objetos de este SDK no realizan la validación de los datos de los fotogramas ID3.</span><span class="sxs-lookup"><span data-stu-id="a0fc8-113">Unless otherwise noted, no validation of ID3 frame data is performed by the objects of this SDK.</span></span> <span data-ttu-id="a0fc8-114">Por ejemplo, el atributo de metadatos de [**WM/letra \_ sincronizado**](wm-lyrics-synchronised.md) almacena la letra de la canción con las marcas de tiempo correspondientes.</span><span class="sxs-lookup"><span data-stu-id="a0fc8-114">For example, the metadata attribute [**WM/Lyrics\_Synchronised**](wm-lyrics-synchronised.md) stores the song lyrics with corresponding time stamps.</span></span> <span data-ttu-id="a0fc8-115">Al escribir un atributo de **WM/letra \_ sincronizado** , los objetos de este SDK no comprobarán para asegurarse de que las marcas de tiempo están en orden cronológico o realizan la validación de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="a0fc8-115">When writing a **WM/Lyrics\_Synchronised** attribute, the objects of this SDK will not check to ensure that the time stamps are in chronological order or perform validation of any kind.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0fc8-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0fc8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0fc8-117">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="a0fc8-117">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="a0fc8-118">**Características de metadatos**</span><span class="sxs-lookup"><span data-stu-id="a0fc8-118">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="a0fc8-119">**Trabajar con metadatos**</span><span class="sxs-lookup"><span data-stu-id="a0fc8-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




