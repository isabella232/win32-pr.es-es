---
description: 'MFPKEY_COLORCONV_MODE propiedad : especifica si el flujo de entrada está entrelazado.'
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: MFPKEY_COLORCONV_MODE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3f2d6256c4d7a9410264fb18703eea251e9c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087583"
---
# <a name="mfpkey_colorconv_mode-property"></a><span data-ttu-id="20bb5-103">Propiedad MFPKEY \_ COLORCONV \_ MODE</span><span class="sxs-lookup"><span data-stu-id="20bb5-103">MFPKEY\_COLORCONV\_MODE Property</span></span>

<span data-ttu-id="20bb5-104">Especifica si el flujo de entrada está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="20bb5-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="20bb5-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="20bb5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="20bb5-106">Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)</span><span class="sxs-lookup"><span data-stu-id="20bb5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="20bb5-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="20bb5-107">Data Type</span></span>

<span data-ttu-id="20bb5-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="20bb5-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="20bb5-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="20bb5-109">Default Value</span></span>

<span data-ttu-id="20bb5-110">Calculado por el DSP del vídeo de origen.</span><span class="sxs-lookup"><span data-stu-id="20bb5-110">Computed by the DSP from the source video.</span></span>

## <a name="applies-to"></a><span data-ttu-id="20bb5-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="20bb5-111">Applies To</span></span>

-   [<span data-ttu-id="20bb5-112">DSP del convertidor de colores</span><span class="sxs-lookup"><span data-stu-id="20bb5-112">Color Converter DSP</span></span>](colorconverter.md)

## <a name="remarks"></a><span data-ttu-id="20bb5-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20bb5-113">Remarks</span></span>

<span data-ttu-id="20bb5-114">Use uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="20bb5-114">Use one of the following values.</span></span>



| <span data-ttu-id="20bb5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="20bb5-115">Value</span></span> | <span data-ttu-id="20bb5-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="20bb5-116">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="20bb5-117">0</span><span class="sxs-lookup"><span data-stu-id="20bb5-117">0</span></span>     | <span data-ttu-id="20bb5-118">progresivo</span><span class="sxs-lookup"><span data-stu-id="20bb5-118">Progressive</span></span> |
| <span data-ttu-id="20bb5-119">2</span><span class="sxs-lookup"><span data-stu-id="20bb5-119">2</span></span>     | <span data-ttu-id="20bb5-120">Interlaced</span><span class="sxs-lookup"><span data-stu-id="20bb5-120">Interlaced</span></span>  |



 

<span data-ttu-id="20bb5-121">Si no se establece esta propiedad, el DSP usa el tipo de medio de entrada para determinar si el vídeo está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="20bb5-121">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="20bb5-122">Puede establecer esta propiedad para invalidar la configuración del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="20bb5-122">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="20bb5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20bb5-123">Requirements</span></span>



| <span data-ttu-id="20bb5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="20bb5-124">Requirement</span></span> | <span data-ttu-id="20bb5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="20bb5-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20bb5-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20bb5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="20bb5-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="20bb5-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="20bb5-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20bb5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="20bb5-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="20bb5-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20bb5-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20bb5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="20bb5-131"><dt>Wmcodecdsp.h</dt></span><span class="sxs-lookup"><span data-stu-id="20bb5-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20bb5-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="20bb5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20bb5-133">Media Foundation propiedades</span><span class="sxs-lookup"><span data-stu-id="20bb5-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
