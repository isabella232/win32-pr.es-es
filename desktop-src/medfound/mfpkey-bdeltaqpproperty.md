---
description: Especifica el incremento diferencial entre el cuantificador de imágenes del marco de anclaje y el cuantificador de imágenes del fotograma B.
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: Propiedad MFPKEY_BDELTAQP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba1ca7d30e17841badeda0312f77471116a8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697142"
---
# <a name="mfpkey_bdeltaqp-property"></a><span data-ttu-id="2caca-103">\_Propiedad BDELTAQP de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="2caca-103">MFPKEY\_BDELTAQP Property</span></span>

<span data-ttu-id="2caca-104">Especifica el incremento diferencial entre el cuantificador de imágenes del marco de anclaje y el cuantificador de imágenes del fotograma B.</span><span class="sxs-lookup"><span data-stu-id="2caca-104">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2caca-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2caca-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2caca-106">g \_ wszWMVCBDeltaQP</span><span class="sxs-lookup"><span data-stu-id="2caca-106">g\_wszWMVCBDeltaQP</span></span>

## <a name="data-type"></a><span data-ttu-id="2caca-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2caca-107">Data Type</span></span>

<span data-ttu-id="2caca-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2caca-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="2caca-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2caca-109">Default Value</span></span>

<span data-ttu-id="2caca-110">0</span><span class="sxs-lookup"><span data-stu-id="2caca-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="2caca-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2caca-111">Remarks</span></span>

<span data-ttu-id="2caca-112">El cuantificador de imágenes (QP) es una medida de la compresión de un fotograma.</span><span class="sxs-lookup"><span data-stu-id="2caca-112">Picture quantizer (QP) is a measurement of how compressed a frame is.</span></span> <span data-ttu-id="2caca-113">Los valores más altos representan mayores proporciones de compresión.</span><span class="sxs-lookup"><span data-stu-id="2caca-113">Higher values represent higher compression ratios.</span></span> <span data-ttu-id="2caca-114">La QP se puede establecer en incrementos de punto medio.</span><span class="sxs-lookup"><span data-stu-id="2caca-114">The QP can be set in half-point increments.</span></span> <span data-ttu-id="2caca-115">Un fotograma B normalmente se comprime en una QP igual que o 0,5 más arriba que el valor de QP del fotograma del delimitador.</span><span class="sxs-lookup"><span data-stu-id="2caca-115">A B-frame is typically compressed at a QP the same as or 0.5 higher than the anchor frame's QP.</span></span> <span data-ttu-id="2caca-116">Al especificar una diferencia de QP de fotogramas B superior a 0, es posible comprimir los fotogramas B con una relación de compresión incluso mayor.</span><span class="sxs-lookup"><span data-stu-id="2caca-116">By specifying a B-frame QP delta higher than 0, it is possible to compress B-frames at an even higher compression ratio.</span></span>

<span data-ttu-id="2caca-117">La diferencia de fotogramas Delta QP solo se puede establecer en incrementos de punto entero.</span><span class="sxs-lookup"><span data-stu-id="2caca-117">The B-frame delta QP can be set only in whole-point increments.</span></span> <span data-ttu-id="2caca-118">Esta propiedad debe establecerse en un valor entero comprendido entre 0 y 31.</span><span class="sxs-lookup"><span data-stu-id="2caca-118">This property must be set to an integer value from 0 to 31.</span></span> <span data-ttu-id="2caca-119">El valor recomendado es 1.</span><span class="sxs-lookup"><span data-stu-id="2caca-119">The recommended value is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2caca-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2caca-120">Requirements</span></span>



| <span data-ttu-id="2caca-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2caca-121">Requirement</span></span> | <span data-ttu-id="2caca-122">Value</span><span class="sxs-lookup"><span data-stu-id="2caca-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2caca-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2caca-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2caca-124">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2caca-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2caca-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2caca-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2caca-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2caca-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2caca-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2caca-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2caca-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2caca-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2caca-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2caca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2caca-130">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2caca-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




