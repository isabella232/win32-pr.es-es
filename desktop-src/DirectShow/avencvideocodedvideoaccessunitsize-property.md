---
description: Especifica el tamaño de las unidades de acceso al vídeo, en bytes. Esta propiedad solo se aplica a los modos de control de velocidad de bits variable (VBR).
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: Propiedad AVEncVideoCodedVideoAccessUnitSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be3a6e499749d862fdcc63f28b1a9a02f476d1c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997656"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a><span data-ttu-id="7ecd8-104">Propiedad AVEncVideoCodedVideoAccessUnitSize</span><span class="sxs-lookup"><span data-stu-id="7ecd8-104">AVEncVideoCodedVideoAccessUnitSize property</span></span>

<span data-ttu-id="7ecd8-105">Especifica el tamaño de las unidades de acceso al vídeo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="7ecd8-105">Specifies the size of the video access units, in bytes.</span></span> <span data-ttu-id="7ecd8-106">Esta propiedad solo se aplica a los modos de control de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="7ecd8-106">This property applies only to variable bit rate (VBR) control modes.</span></span>

<span data-ttu-id="7ecd8-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7ecd8-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="7ecd8-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7ecd8-108">Data type</span></span>

<span data-ttu-id="7ecd8-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="7ecd8-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7ecd8-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="7ecd8-110">Property GUID</span></span>

<span data-ttu-id="7ecd8-111">**CODECAPI \_ AVEncVideoCodedVideoAccessUnitSize**</span><span class="sxs-lookup"><span data-stu-id="7ecd8-111">**CODECAPI\_AVEncVideoCodedVideoAccessUnitSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="7ecd8-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7ecd8-112">Property value</span></span>

<span data-ttu-id="7ecd8-113">Esta propiedad se devuelve como un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="7ecd8-113">This property is returned as a range of values.</span></span> <span data-ttu-id="7ecd8-114">Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="7ecd8-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ecd8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ecd8-115">Requirements</span></span>



| <span data-ttu-id="7ecd8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ecd8-116">Requirement</span></span> | <span data-ttu-id="7ecd8-117">Value</span><span class="sxs-lookup"><span data-stu-id="7ecd8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ecd8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ecd8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7ecd8-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="7ecd8-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7ecd8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ecd8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7ecd8-121">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="7ecd8-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7ecd8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ecd8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ecd8-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ecd8-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ecd8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ecd8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ecd8-125">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="7ecd8-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7ecd8-126">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="7ecd8-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




