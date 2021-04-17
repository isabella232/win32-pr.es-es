---
title: Interfaz IWMPMetadataPicture (VB y C) (WMP. h)
description: Proporciona propiedades para obtener información sobre la imagen contenida en un archivo multimedia digital representado por un atributo WM/Picturemetadata.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- IWMPMetadataPicture (VB y C) interfaz de Windows Media Player
- IWMPMetadataPicture (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b462c431a136745974dcde5716c3bd81226f15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690770"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a><span data-ttu-id="cf956-105">Interfaz IWMPMetadataPicture (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="cf956-105">IWMPMetadataPicture (VB and C#) interface</span></span>

<span data-ttu-id="cf956-106">Proporciona propiedades para obtener información acerca de la imagen contenida en un archivo multimedia digital representado por un atributo de metadatos de [**WM/imagen**](/windows/desktop/wmformat/wmpicture).</span><span class="sxs-lookup"><span data-stu-id="cf956-106">Provides properties for getting information about the image contained in a digital media file that is represented by a [**WM/Picture**](/windows/desktop/wmformat/wmpicture)metadata attribute.</span></span> <span data-ttu-id="cf956-107">Este atributo corresponde a las imágenes de carátulas de álbum contenidas en un archivo multimedia digital, no a la carátula de álbum descargada a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="cf956-107">This attribute corresponds to album art images contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="cf956-108">La interfaz **IWMPMetadataPicture** expone las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="cf956-108">The **IWMPMetadataPicture** interface exposes the following properties.</span></span>



| <span data-ttu-id="cf956-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf956-109">Property</span></span>                                                                                   | <span data-ttu-id="cf956-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf956-110">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="cf956-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf956-111">**Description**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | <span data-ttu-id="cf956-112">Obtiene la descripción de la imagen representada por el atributo de metadatos.</span><span class="sxs-lookup"><span data-stu-id="cf956-112">Gets the description of the image represented by the metadata attribute.</span></span>  |
| [<span data-ttu-id="cf956-113">**mimeType**</span><span class="sxs-lookup"><span data-stu-id="cf956-113">**mimeType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | <span data-ttu-id="cf956-114">Obtiene el tipo MIME de la imagen representada por el atributo de metadatos.</span><span class="sxs-lookup"><span data-stu-id="cf956-114">Gets the MIME type of the image represented by the metadata attribute.</span></span>    |
| [<span data-ttu-id="cf956-115">**Tal**</span><span class="sxs-lookup"><span data-stu-id="cf956-115">**pictureType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | <span data-ttu-id="cf956-116">Obtiene el tipo de imagen de la imagen representada por el atributo de metadatos.</span><span class="sxs-lookup"><span data-stu-id="cf956-116">Gets the picture type of the image represented by the metadata attribute.</span></span> |
| [<span data-ttu-id="cf956-117">**URL**</span><span class="sxs-lookup"><span data-stu-id="cf956-117">**URL**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | <span data-ttu-id="cf956-118">Exclusivamente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="cf956-118">Internal use only.</span></span>                                                        |



 

<span data-ttu-id="cf956-119">Obtenga una interfaz **IWMPMetadataPicture** pasando el nombre de atributo [**WM/Picture**](/windows/desktop/wmformat/wmpicture) al método siguiente y convirtiendo el objeto que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="cf956-119">Get an **IWMPMetadataPicture** interface by passing in the attribute name [**WM/Picture**](/windows/desktop/wmformat/wmpicture) to the following method and casting the object that is returned.</span></span>



| <span data-ttu-id="cf956-120">Interfaz</span><span class="sxs-lookup"><span data-stu-id="cf956-120">Interface</span></span>                                  | <span data-ttu-id="cf956-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf956-121">Property</span></span>                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf956-122">**IWMPMedia3**</span><span class="sxs-lookup"><span data-stu-id="cf956-122">**IWMPMedia3**</span></span>](iwmpmedia3--vb-and-c.md) | [<span data-ttu-id="cf956-123">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="cf956-123">**getItemInfoByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a><span data-ttu-id="cf956-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf956-124">Members</span></span>

<span data-ttu-id="cf956-125">La interfaz **IWMPMetadataPicture (VB y C#)** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="cf956-125">The **IWMPMetadataPicture (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf956-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf956-126">Requirements</span></span>



| <span data-ttu-id="cf956-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf956-127">Requirement</span></span> | <span data-ttu-id="cf956-128">Value</span><span class="sxs-lookup"><span data-stu-id="cf956-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cf956-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf956-129">Header</span></span><br/> | <dl> <span data-ttu-id="cf956-130"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf956-130"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf956-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf956-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf956-132">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="cf956-132">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

