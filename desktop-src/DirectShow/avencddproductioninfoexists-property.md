---
description: Especifica la marca de información de producción de audio en una secuencia de audio Dolby digital. Esta propiedad se aplica a los codificadores de audio Dolby digital.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Propiedad AVEncDDProductionInfoExists (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5069c8d30f0266b0727f735ede822be491c4a4a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686390"
---
# <a name="avencddproductioninfoexists-property"></a><span data-ttu-id="3f2c3-104">Propiedad AVEncDDProductionInfoExists</span><span class="sxs-lookup"><span data-stu-id="3f2c3-104">AVEncDDProductionInfoExists property</span></span>

<span data-ttu-id="3f2c3-105">Especifica la marca de información de producción de audio en una secuencia de audio Dolby digital.</span><span class="sxs-lookup"><span data-stu-id="3f2c3-105">Specifies the audio production information flag in a Dolby Digital audio stream.</span></span> <span data-ttu-id="3f2c3-106">Esta propiedad se aplica a los codificadores de audio Dolby digital.</span><span class="sxs-lookup"><span data-stu-id="3f2c3-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="3f2c3-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3f2c3-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="3f2c3-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3f2c3-108">Data type</span></span>

<span data-ttu-id="3f2c3-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="3f2c3-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3f2c3-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="3f2c3-110">Property GUID</span></span>

<span data-ttu-id="3f2c3-111">**CODECAPI \_ AVEncDDProductionInfoExists**</span><span class="sxs-lookup"><span data-stu-id="3f2c3-111">**CODECAPI\_AVEncDDProductionInfoExists**</span></span>

## <a name="remarks"></a><span data-ttu-id="3f2c3-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f2c3-112">Remarks</span></span>

<span data-ttu-id="3f2c3-113">Si el valor es **Variant \_ true**, los valores de nivel de combinación y tipo de sala son válidos.</span><span class="sxs-lookup"><span data-stu-id="3f2c3-113">If the value is **VARIANT\_TRUE**, the mixing level and room type settings are valid.</span></span> <span data-ttu-id="3f2c3-114">Especifique estos valores con las propiedades [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) y [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) .</span><span class="sxs-lookup"><span data-stu-id="3f2c3-114">Specify these settings with the [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) and [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f2c3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f2c3-115">Requirements</span></span>



| <span data-ttu-id="3f2c3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f2c3-116">Requirement</span></span> | <span data-ttu-id="3f2c3-117">Value</span><span class="sxs-lookup"><span data-stu-id="3f2c3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f2c3-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f2c3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3f2c3-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="3f2c3-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3f2c3-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f2c3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3f2c3-121">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="3f2c3-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3f2c3-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f2c3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f2c3-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f2c3-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f2c3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f2c3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f2c3-125">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="3f2c3-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="3f2c3-126">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="3f2c3-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




