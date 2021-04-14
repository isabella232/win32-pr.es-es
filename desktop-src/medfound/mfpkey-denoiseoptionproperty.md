---
description: Especifica si el códec usará el filtro de ruido al codificar.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: Propiedad MFPKEY_DENOISEOPTION (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f318e294f69095758fe300fce19043c23cf376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648310"
---
# <a name="mfpkey_denoiseoption-property"></a><span data-ttu-id="d8488-103">\_Propiedad DENOISEOPTION de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="d8488-103">MFPKEY\_DENOISEOPTION Property</span></span>

<span data-ttu-id="d8488-104">Especifica si el códec usará el filtro de ruido al codificar.</span><span class="sxs-lookup"><span data-stu-id="d8488-104">Specifies whether the codec will use the noise filter when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d8488-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d8488-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d8488-106">g \_ wszWMVCDenoiseOption</span><span class="sxs-lookup"><span data-stu-id="d8488-106">g\_wszWMVCDenoiseOption</span></span>

## <a name="data-type"></a><span data-ttu-id="d8488-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d8488-107">Data Type</span></span>

<span data-ttu-id="d8488-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="d8488-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="d8488-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="d8488-109">Default Value</span></span>

<span data-ttu-id="d8488-110">false</span><span class="sxs-lookup"><span data-stu-id="d8488-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="d8488-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8488-111">Remarks</span></span>

<span data-ttu-id="d8488-112">El filtro de ruido puede mejorar la calidad de los orígenes de vídeo ruidosos, como la película que contiene una gran cantidad de grano o vídeo captado en baja luz.</span><span class="sxs-lookup"><span data-stu-id="d8488-112">The noise filter can improve the quality of noisy video sources, such as film containing lots of grain or video shot in low light.</span></span> <span data-ttu-id="d8488-113">Este filtro se puede usar en escenarios de codificación en directo donde el preprocesamiento externo no es una opción.</span><span class="sxs-lookup"><span data-stu-id="d8488-113">This filter can be used in live encoding scenarios where external preprocessing is not an option.</span></span>

<span data-ttu-id="d8488-114">Este filtro debe estar deshabilitado para los orígenes de vídeo limpios, ya que puede reducir la calidad de la imagen cuando la calidad es buena para empezar.</span><span class="sxs-lookup"><span data-stu-id="d8488-114">This filter should be disabled for clean video sources since it can reduce image quality when the quality is good to start with.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8488-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8488-115">Requirements</span></span>



| <span data-ttu-id="d8488-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8488-116">Requirement</span></span> | <span data-ttu-id="d8488-117">Value</span><span class="sxs-lookup"><span data-stu-id="d8488-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8488-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8488-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d8488-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d8488-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d8488-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8488-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d8488-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8488-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d8488-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8488-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8488-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8488-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8488-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8488-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8488-125">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d8488-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




