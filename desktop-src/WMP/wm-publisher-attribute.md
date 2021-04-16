---
title: Atributo de WM/publicador
description: El atributo WM/publicador es el nombre de la empresa que publicó el contenido.
ms.assetid: 5f3aa5de-237e-449c-918e-8750481adc6f
keywords:
- Windows atributo de WM/publicador Media Player
topic_type:
- apiref
api_name:
- WM/Publisher
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00bd0d2ab2b6d886639cffa1df0770dfe329f7f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718865"
---
# <a name="wmpublisher-attribute"></a><span data-ttu-id="2cb14-104">Atributo de WM/publicador</span><span class="sxs-lookup"><span data-stu-id="2cb14-104">WM/Publisher Attribute</span></span>

<span data-ttu-id="2cb14-105">El atributo **WM/publicador** es el nombre de la empresa que publicó el contenido.</span><span class="sxs-lookup"><span data-stu-id="2cb14-105">The **WM/Publisher** attribute is the name of the company that published the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="2cb14-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="2cb14-106">Applies To</span></span>

-   [<span data-ttu-id="2cb14-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="2cb14-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="2cb14-108">Listas de reproducción de CD</span><span class="sxs-lookup"><span data-stu-id="2cb14-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="2cb14-109">Pistas de CD</span><span class="sxs-lookup"><span data-stu-id="2cb14-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="2cb14-110">Atributos de archivo de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="2cb14-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="2cb14-111">DVDs</span><span class="sxs-lookup"><span data-stu-id="2cb14-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="2cb14-112">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="2cb14-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="2cb14-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2cb14-113">Remarks</span></span>

<span data-ttu-id="2cb14-114">Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="2cb14-114">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="2cb14-115">**Label**, **ReleasedBy** y **Studio** son alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="2cb14-115">**Label**, **ReleasedBy**, and **Studio** are aliases for this attribute.</span></span>

<span data-ttu-id="2cb14-116">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMPublisher.</span><span class="sxs-lookup"><span data-stu-id="2cb14-116">The Windows Media Format SDK constant for this attribute is g\_wszWMPublisher.</span></span>

<span data-ttu-id="2cb14-117">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="2cb14-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cb14-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cb14-118">Requirements</span></span>



| <span data-ttu-id="2cb14-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cb14-119">Requirement</span></span> | <span data-ttu-id="2cb14-120">Value</span><span class="sxs-lookup"><span data-stu-id="2cb14-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="2cb14-121">Versión</span><span class="sxs-lookup"><span data-stu-id="2cb14-121">Version</span></span><br/> | <span data-ttu-id="2cb14-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="2cb14-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2cb14-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cb14-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb14-124">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="2cb14-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





