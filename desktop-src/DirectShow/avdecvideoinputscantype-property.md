---
description: Especifica cómo se entrelaza la secuencia de vídeo descodificada.
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: Propiedad AVDecVideoInputScanType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 560db1cd1cf0238fc9e50257f2f24559e9a94c8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906733"
---
# <a name="avdecvideoinputscantype-property"></a><span data-ttu-id="017af-103">Propiedad AVDecVideoInputScanType</span><span class="sxs-lookup"><span data-stu-id="017af-103">AVDecVideoInputScanType property</span></span>

<span data-ttu-id="017af-104">Especifica cómo se entrelaza la secuencia de vídeo descodificada.</span><span class="sxs-lookup"><span data-stu-id="017af-104">Specifies how the decoded video stream is interlaced.</span></span>

<span data-ttu-id="017af-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="017af-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="017af-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="017af-106">Data type</span></span>

<span data-ttu-id="017af-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="017af-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="017af-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="017af-108">Property GUID</span></span>

<span data-ttu-id="017af-109">**CODECAPI \_ AVDecVideoInputScanType**</span><span class="sxs-lookup"><span data-stu-id="017af-109">**CODECAPI\_AVDecVideoInputScanType**</span></span>

## <a name="property-value"></a><span data-ttu-id="017af-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="017af-110">Property value</span></span>

<span data-ttu-id="017af-111">El valor de esta propiedad es un miembro de la enumeración [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) .</span><span class="sxs-lookup"><span data-stu-id="017af-111">The value of this property is a member of the [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="017af-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="017af-112">Remarks</span></span>

<span data-ttu-id="017af-113">Los 16 bits superiores del valor contienen el ancho y los 16 bits inferiores contienen el alto.</span><span class="sxs-lookup"><span data-stu-id="017af-113">The upper 16 bits of the value contain the width, and the lower 16 bits contain the height.</span></span>

## <a name="requirements"></a><span data-ttu-id="017af-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="017af-114">Requirements</span></span>



| <span data-ttu-id="017af-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="017af-115">Requirement</span></span> | <span data-ttu-id="017af-116">Value</span><span class="sxs-lookup"><span data-stu-id="017af-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="017af-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="017af-117">Minimum supported client</span></span><br/> | <span data-ttu-id="017af-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="017af-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="017af-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="017af-119">Minimum supported server</span></span><br/> | <span data-ttu-id="017af-120">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="017af-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="017af-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="017af-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="017af-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="017af-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="017af-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="017af-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="017af-124">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="017af-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="017af-125">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="017af-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

