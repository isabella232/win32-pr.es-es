---
title: Atributo WM/TrackNumber
description: El atributo WM/TrackNumber es el número de pista del elemento en el álbum en el que se liberó originalmente.
ms.assetid: d1fc5bac-c440-470f-be5c-5aca74aee99e
keywords:
- Media Player de Windows de atributos de WM/TrackNumber
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd9adf3a939a5087ee270e8bef4d4d510b678ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690566"
---
# <a name="wmtracknumber-attribute"></a><span data-ttu-id="ad86e-104">Atributo WM/TrackNumber</span><span class="sxs-lookup"><span data-stu-id="ad86e-104">WM/TrackNumber Attribute</span></span>

<span data-ttu-id="ad86e-105">El atributo **WM/TrackNumber** es el número de pista del elemento en el álbum en el que se liberó originalmente.</span><span class="sxs-lookup"><span data-stu-id="ad86e-105">The **WM/TrackNumber** attribute is the track number of the item on the album on which it was originally released.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ad86e-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="ad86e-106">Applies To</span></span>

-   [<span data-ttu-id="ad86e-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="ad86e-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="ad86e-108">Atributos de archivo de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="ad86e-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="ad86e-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad86e-109">Remarks</span></span>

<span data-ttu-id="ad86e-110">Este atributo se almacena en la biblioteca y en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="ad86e-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="ad86e-111">Los números de seguimiento de un álbum empiezan en 1.</span><span class="sxs-lookup"><span data-stu-id="ad86e-111">Track numbers for an album start at 1.</span></span>

<span data-ttu-id="ad86e-112">**OriginalIndex** y **OriginalIndexLeft** son alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="ad86e-112">**OriginalIndex** and **OriginalIndexLeft** are aliases for this attribute.</span></span>

<span data-ttu-id="ad86e-113">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMTrackNumber.</span><span class="sxs-lookup"><span data-stu-id="ad86e-113">The Windows Media Format SDK constant for this attribute is g\_wszWMTrackNumber.</span></span>

<span data-ttu-id="ad86e-114">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="ad86e-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad86e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad86e-115">Requirements</span></span>



| <span data-ttu-id="ad86e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad86e-116">Requirement</span></span> | <span data-ttu-id="ad86e-117">Value</span><span class="sxs-lookup"><span data-stu-id="ad86e-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="ad86e-118">Versión</span><span class="sxs-lookup"><span data-stu-id="ad86e-118">Version</span></span><br/> | <span data-ttu-id="ad86e-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="ad86e-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad86e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad86e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad86e-121">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="ad86e-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





