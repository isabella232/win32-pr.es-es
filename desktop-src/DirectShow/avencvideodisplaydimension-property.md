---
description: Especifica el tamaño de la secuencia de vídeo cuando se descodifica.
ms.assetid: db7b101a-5ff8-4a62-b9e2-d05fcdc44b3d
title: Propiedad AVEncVideoDisplayDimension (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e5f611525e68f6f47c442c6e733c6c3e7de14d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659259"
---
# <a name="avencvideodisplaydimension-property"></a><span data-ttu-id="fdbdc-103">Propiedad AVEncVideoDisplayDimension</span><span class="sxs-lookup"><span data-stu-id="fdbdc-103">AVEncVideoDisplayDimension property</span></span>

<span data-ttu-id="fdbdc-104">Especifica el tamaño de la secuencia de vídeo cuando se descodifica.</span><span class="sxs-lookup"><span data-stu-id="fdbdc-104">Specifies the size of the video stream when it is decoded.</span></span>

<span data-ttu-id="fdbdc-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fdbdc-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fdbdc-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fdbdc-106">Data type</span></span>

<span data-ttu-id="fdbdc-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="fdbdc-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fdbdc-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="fdbdc-108">Property GUID</span></span>

<span data-ttu-id="fdbdc-109">**CODECAPI \_ AVEncVideoDisplayDimension**</span><span class="sxs-lookup"><span data-stu-id="fdbdc-109">**CODECAPI\_AVEncVideoDisplayDimension**</span></span>

## <a name="property-value"></a><span data-ttu-id="fdbdc-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fdbdc-110">Property value</span></span>

<span data-ttu-id="fdbdc-111">Los 16 bits superiores del valor contienen el ancho, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fdbdc-111">The upper 16 bits of the value contain the width, in pixels.</span></span> <span data-ttu-id="fdbdc-112">Los 16 bits inferiores contienen el alto, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fdbdc-112">The lower 16 bits contain the height, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdbdc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdbdc-113">Requirements</span></span>



| <span data-ttu-id="fdbdc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdbdc-114">Requirement</span></span> | <span data-ttu-id="fdbdc-115">Value</span><span class="sxs-lookup"><span data-stu-id="fdbdc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdbdc-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdbdc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fdbdc-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="fdbdc-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fdbdc-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdbdc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fdbdc-119">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="fdbdc-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fdbdc-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fdbdc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdbdc-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdbdc-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdbdc-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdbdc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdbdc-123">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="fdbdc-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fdbdc-124">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="fdbdc-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




