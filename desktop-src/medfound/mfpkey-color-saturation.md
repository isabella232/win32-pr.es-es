---
description: Ajusta la saturación.
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: Propiedad MFPKEY_COLOR_SATURATION (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496b1f017ceff6ab4bd01ce01ccfd5da0759befc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544939"
---
# <a name="mfpkey_color_saturation-property"></a><span data-ttu-id="f0c12-103">\_Propiedad saturación de color MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="f0c12-103">MFPKEY\_COLOR\_SATURATION Property</span></span>

<span data-ttu-id="f0c12-104">Ajusta la saturación.</span><span class="sxs-lookup"><span data-stu-id="f0c12-104">Adjusts the saturation.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f0c12-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f0c12-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f0c12-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="f0c12-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f0c12-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f0c12-107">Data Type</span></span>

<span data-ttu-id="f0c12-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f0c12-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="f0c12-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f0c12-109">Default Value</span></span>

<span data-ttu-id="f0c12-110">0</span><span class="sxs-lookup"><span data-stu-id="f0c12-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="f0c12-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="f0c12-111">Applies To</span></span>

-   [<span data-ttu-id="f0c12-112">DSP de transformación de control de color</span><span class="sxs-lookup"><span data-stu-id="f0c12-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="f0c12-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0c12-113">Remarks</span></span>

<span data-ttu-id="f0c12-114">El ajuste de saturación se realiza multiplicando los valores CB y CR por una constante.</span><span class="sxs-lookup"><span data-stu-id="f0c12-114">Saturation adjustment is performed by multiplying the Cb and Cr values by a constant.</span></span>

<span data-ttu-id="f0c12-115">Esta propiedad tiene un intervalo de-127 a 127.</span><span class="sxs-lookup"><span data-stu-id="f0c12-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="f0c12-116">Cero indica que no hay ningún cambio en la saturación.</span><span class="sxs-lookup"><span data-stu-id="f0c12-116">Zero indicates no change in saturation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c12-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0c12-117">Requirements</span></span>



| <span data-ttu-id="f0c12-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0c12-118">Requirement</span></span> | <span data-ttu-id="f0c12-119">Value</span><span class="sxs-lookup"><span data-stu-id="f0c12-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c12-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0c12-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c12-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f0c12-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f0c12-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0c12-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c12-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0c12-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0c12-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0c12-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0c12-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0c12-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0c12-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0c12-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c12-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0c12-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
