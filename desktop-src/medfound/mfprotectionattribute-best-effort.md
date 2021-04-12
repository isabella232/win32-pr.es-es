---
description: Se establece como un atributo para un objeto IMFOutputSchema.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: MFPROTECTIONATTRIBUTE_BEST_EFFORT atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276225"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a><span data-ttu-id="dedd1-103">\_Atributo de mejor esfuerzo de MFPROTECTIONATTRIBUTE \_</span><span class="sxs-lookup"><span data-stu-id="dedd1-103">MFPROTECTIONATTRIBUTE\_BEST\_EFFORT attribute</span></span>

<span data-ttu-id="dedd1-104">Se establece como un atributo para un objeto [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .</span><span class="sxs-lookup"><span data-stu-id="dedd1-104">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span> <span data-ttu-id="dedd1-105">Si este atributo está presente, se omite un error al intentar aplicar la protección.</span><span class="sxs-lookup"><span data-stu-id="dedd1-105">If this attribute is present, a failed attempt to apply the protection is ignored.</span></span> <span data-ttu-id="dedd1-106">Si el valor del atributo asociado es **true**, se debe aplicar el esquema de protección con el atributo de [conmutación por \_ error \_ de MFPROTECTIONATTRIBUTE](mfprotectionattribute-fail-over.md) .</span><span class="sxs-lookup"><span data-stu-id="dedd1-106">If the associated attribute value is **TRUE**, the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute should be applied.</span></span>

## <a name="data-type"></a><span data-ttu-id="dedd1-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="dedd1-107">Data type</span></span>

<span data-ttu-id="dedd1-108">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="dedd1-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dedd1-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dedd1-109">Remarks</span></span>

<span data-ttu-id="dedd1-110">Si **es true**, aplique el esquema de protección con el atributo de [ \_ conmutación \_ por error de MFPROTECTIONATTRIBUTE](mfprotectionattribute-fail-over.md) si se produce un error al establecer esta protección.</span><span class="sxs-lookup"><span data-stu-id="dedd1-110">If **TRUE**, enforce the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute if setting this protection fails.</span></span>

<span data-ttu-id="dedd1-111">Se establece como un atributo para un objeto [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .</span><span class="sxs-lookup"><span data-stu-id="dedd1-111">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="dedd1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dedd1-112">Requirements</span></span>



| <span data-ttu-id="dedd1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="dedd1-113">Requirement</span></span> | <span data-ttu-id="dedd1-114">Value</span><span class="sxs-lookup"><span data-stu-id="dedd1-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dedd1-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dedd1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dedd1-116">\[Solo aplicaciones para UWP de Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dedd1-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dedd1-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dedd1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dedd1-118">\[Solo aplicaciones para UWP de Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dedd1-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dedd1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dedd1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="dedd1-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dedd1-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dedd1-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="dedd1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dedd1-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dedd1-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dedd1-123">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="dedd1-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




