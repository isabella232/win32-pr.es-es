---
title: Objeto MetadataPicture
description: El objeto MetadataPicture proporciona una manera de recuperar los valores del atributo de metadatos de WM/imagen. Este atributo corresponde a la carátula de álbum contenida en un archivo multimedia digital, no a la carátula de álbum descargada a través de Internet.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- Objeto MetadataPicture Media Player de Windows
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 892b162ba05ab43740565c849b00bc4e3c52aad6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488130"
---
# <a name="metadatapicture-object"></a><span data-ttu-id="a1b87-105">Objeto MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="a1b87-105">MetadataPicture Object</span></span>

<span data-ttu-id="a1b87-106">El objeto **MetadataPicture** proporciona una manera de recuperar los valores del atributo de metadatos de [**WM/imagen**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) .</span><span class="sxs-lookup"><span data-stu-id="a1b87-106">The **MetadataPicture** object provides a way to retrieve the values of the [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) metadata attribute.</span></span> <span data-ttu-id="a1b87-107">Este atributo corresponde a la carátula de álbum contenida en un archivo multimedia digital, no a la carátula de álbum descargada a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="a1b87-107">This attribute corresponds to album art contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="a1b87-108">El objeto **MetadataPicture** admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="a1b87-108">The **MetadataPicture** object supports the following properties.</span></span>



| <span data-ttu-id="a1b87-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a1b87-109">Property</span></span>                                           | <span data-ttu-id="a1b87-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1b87-110">Description</span></span>                                       |
|----------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="a1b87-111">**denominación**</span><span class="sxs-lookup"><span data-stu-id="a1b87-111">**description**</span></span>](metadatapicture-description.md) | <span data-ttu-id="a1b87-112">Recupera una descripción de la imagen de metadatos.</span><span class="sxs-lookup"><span data-stu-id="a1b87-112">Retrieves a description of the metadata image.</span></span>    |
| [<span data-ttu-id="a1b87-113">**mimeType**</span><span class="sxs-lookup"><span data-stu-id="a1b87-113">**mimeType**</span></span>](metadatapicture-mimetype.md)       | <span data-ttu-id="a1b87-114">Recupera el tipo MIME de la imagen de metadatos.</span><span class="sxs-lookup"><span data-stu-id="a1b87-114">Retrieves the MIME type of the metadata image.</span></span>    |
| [<span data-ttu-id="a1b87-115">**Tal**</span><span class="sxs-lookup"><span data-stu-id="a1b87-115">**pictureType**</span></span>](metadatapicture-picturetype.md) | <span data-ttu-id="a1b87-116">Recupera el tipo de imagen de la imagen de metadatos.</span><span class="sxs-lookup"><span data-stu-id="a1b87-116">Retrieves the picture type of the metadata image.</span></span> |
| [<span data-ttu-id="a1b87-117">**URL**</span><span class="sxs-lookup"><span data-stu-id="a1b87-117">**URL**</span></span>](metadatapicture-url.md)                 | <span data-ttu-id="a1b87-118">Exclusivamente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="a1b87-118">Internal use only.</span></span>                                |



 

<span data-ttu-id="a1b87-119">Se tiene acceso al objeto **MetadataPicture** mediante el método siguiente.</span><span class="sxs-lookup"><span data-stu-id="a1b87-119">The **MetadataPicture** object is accessed through the following method.</span></span>



| <span data-ttu-id="a1b87-120">Object</span><span class="sxs-lookup"><span data-stu-id="a1b87-120">Object</span></span>                        | <span data-ttu-id="a1b87-121">Método</span><span class="sxs-lookup"><span data-stu-id="a1b87-121">Method</span></span>                                               |
|-------------------------------|------------------------------------------------------|
| [<span data-ttu-id="a1b87-122">**Medios**</span><span class="sxs-lookup"><span data-stu-id="a1b87-122">**Media**</span></span>](media-object.md) | [<span data-ttu-id="a1b87-123">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="a1b87-123">**getItemInfoByType**</span></span>](media-getiteminfobytype.md) |



 

<span data-ttu-id="a1b87-124">`player.currentMedia.getItemInfoByType(name, language, index)`En lo que respecta a la ilustración, se usa en las secciones de sintaxis de referencia.</span><span class="sxs-lookup"><span data-stu-id="a1b87-124">For purposes of illustration, `player.currentMedia.getItemInfoByType(name, language, index)` is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1b87-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1b87-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b87-126">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="a1b87-126">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 