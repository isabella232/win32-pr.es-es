---
description: Especifica si el flujo de entrada está entrelazado.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: Propiedad MFPKEY_COLORCONV_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8c01a6dce595eb270b734947492deea014259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812770"
---
# <a name="mfpkey_colorconv_mode-property"></a><span data-ttu-id="1c795-103">\_Propiedad de modo COLORCONV de MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="1c795-103">MFPKEY\_COLORCONV\_MODE Property</span></span>

<span data-ttu-id="1c795-104">Especifica si el flujo de entrada está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="1c795-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1c795-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1c795-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1c795-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="1c795-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="1c795-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1c795-107">Data Type</span></span>

<span data-ttu-id="1c795-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1c795-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="1c795-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="1c795-109">Default Value</span></span>

<span data-ttu-id="1c795-110">Lo calcula el DSP desde el vídeo de origen.</span><span class="sxs-lookup"><span data-stu-id="1c795-110">Computed by the DSP from the source video.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1c795-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="1c795-111">Applies To</span></span>

-   [<span data-ttu-id="1c795-112">DSP de convertidor de colores</span><span class="sxs-lookup"><span data-stu-id="1c795-112">Color Converter DSP</span></span>](colorconverter.md)

## <a name="remarks"></a><span data-ttu-id="1c795-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c795-113">Remarks</span></span>

<span data-ttu-id="1c795-114">Use uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="1c795-114">Use one of the following values.</span></span>



| <span data-ttu-id="1c795-115">Value</span><span class="sxs-lookup"><span data-stu-id="1c795-115">Value</span></span> | <span data-ttu-id="1c795-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c795-116">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="1c795-117">0</span><span class="sxs-lookup"><span data-stu-id="1c795-117">0</span></span>     | <span data-ttu-id="1c795-118">progresivo</span><span class="sxs-lookup"><span data-stu-id="1c795-118">Progressive</span></span> |
| <span data-ttu-id="1c795-119">2</span><span class="sxs-lookup"><span data-stu-id="1c795-119">2</span></span>     | <span data-ttu-id="1c795-120">Interlaced</span><span class="sxs-lookup"><span data-stu-id="1c795-120">Interlaced</span></span>  |



 

<span data-ttu-id="1c795-121">Si no se establece esta propiedad, el DSP usa el tipo de medio de entrada para determinar si el vídeo está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="1c795-121">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="1c795-122">Puede establecer esta propiedad para invalidar la configuración de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="1c795-122">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c795-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c795-123">Requirements</span></span>



| <span data-ttu-id="1c795-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c795-124">Requirement</span></span> | <span data-ttu-id="1c795-125">Value</span><span class="sxs-lookup"><span data-stu-id="1c795-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c795-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c795-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1c795-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1c795-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1c795-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c795-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1c795-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c795-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c795-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c795-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c795-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c795-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c795-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c795-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c795-133">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c795-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
