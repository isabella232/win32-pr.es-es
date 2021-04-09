---
description: Especifica si el códec debe utilizar el filtrado medio durante la codificación.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: Propiedad MFPKEY_FORCEMEDIANSETTING (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914173"
---
# <a name="mfpkey_forcemediansetting-property"></a><span data-ttu-id="fd835-103">\_Propiedad FORCEMEDIANSETTING de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="fd835-103">MFPKEY\_FORCEMEDIANSETTING Property</span></span>

<span data-ttu-id="fd835-104">Especifica si el códec debe utilizar el filtrado medio durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="fd835-104">Specifies whether the codec should use median filtering during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="fd835-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="fd835-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="fd835-106">g \_ wszWMVCForceMedianSetting</span><span class="sxs-lookup"><span data-stu-id="fd835-106">g\_wszWMVCForceMedianSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="fd835-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fd835-107">Data Type</span></span>

<span data-ttu-id="fd835-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="fd835-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="fd835-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="fd835-109">Default Value</span></span>

<span data-ttu-id="fd835-110">false</span><span class="sxs-lookup"><span data-stu-id="fd835-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="fd835-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd835-111">Remarks</span></span>

<span data-ttu-id="fd835-112">El filtrado medio indica al códec que omita el ruido y el grano al calcular el movimiento entre los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="fd835-112">Median filtering tells the codec to ignore noise and grain when calculating motion between frames.</span></span> <span data-ttu-id="fd835-113">Esto puede mejorar la calidad del vídeo muy ruidoso, pero puede dar lugar a los seguimientos de movimiento (también conocidos como artefactos finales) cuando se aplican al vídeo de origen limpio.</span><span class="sxs-lookup"><span data-stu-id="fd835-113">This can improve the quality of very noisy video, but can lead to motion trails (also known as trailing artifacts) when applied to clean source video.</span></span>

<span data-ttu-id="fd835-114">De forma predeterminada, el códec usa la lógica interna para determinar si se debe usar el filtrado de mediana.</span><span class="sxs-lookup"><span data-stu-id="fd835-114">By default, the codec uses internal logic to determine whether median filtering should be used.</span></span> <span data-ttu-id="fd835-115">Si establece esta propiedad, se invalidará esa lógica.</span><span class="sxs-lookup"><span data-stu-id="fd835-115">If you set this property, that logic will be overridden.</span></span>

> [!Note]  
> <span data-ttu-id="fd835-116">Este filtro no es el mismo que el de los filtros de desenfoque medio que se encuentran en muchas aplicaciones de edición y postprocesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fd835-116">This filter is not the same as median blur filters found in many video editing and post-processing applications.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fd835-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd835-117">Requirements</span></span>



| <span data-ttu-id="fd835-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd835-118">Requirement</span></span> | <span data-ttu-id="fd835-119">Value</span><span class="sxs-lookup"><span data-stu-id="fd835-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd835-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd835-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fd835-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fd835-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fd835-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd835-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fd835-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd835-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fd835-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd835-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd835-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd835-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd835-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd835-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd835-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fd835-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




