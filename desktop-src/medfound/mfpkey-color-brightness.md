---
description: Ajusta el brillo.
ms.assetid: 1b3f56eb-3f22-4120-ba6c-331eccd5d303
title: Propiedad MFPKEY_COLOR_BRIGHTNESS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 685ab934a91f1843183fcfa88bb94c83e602db27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909393"
---
# <a name="mfpkey_color_brightness-property"></a><span data-ttu-id="75d69-103">Propiedad de brillo de \_ color MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="75d69-103">MFPKEY\_COLOR\_BRIGHTNESS Property</span></span>

<span data-ttu-id="75d69-104">Ajusta el brillo.</span><span class="sxs-lookup"><span data-stu-id="75d69-104">Adjusts the brightness.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="75d69-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="75d69-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="75d69-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="75d69-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="75d69-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="75d69-107">Data Type</span></span>

<span data-ttu-id="75d69-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="75d69-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="75d69-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="75d69-109">Default Value</span></span>

<span data-ttu-id="75d69-110">0</span><span class="sxs-lookup"><span data-stu-id="75d69-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="75d69-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="75d69-111">Applies To</span></span>

-   [<span data-ttu-id="75d69-112">DSP de transformación de control de color</span><span class="sxs-lookup"><span data-stu-id="75d69-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="75d69-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75d69-113">Remarks</span></span>

<span data-ttu-id="75d69-114">El ajuste de brillo se realiza agregando un valor al canal de luminancia.</span><span class="sxs-lookup"><span data-stu-id="75d69-114">Brightness adjustment is performed by adding a value to the luma channel.</span></span>

<span data-ttu-id="75d69-115">Esta propiedad tiene un intervalo de-127 a 127.</span><span class="sxs-lookup"><span data-stu-id="75d69-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="75d69-116">Cero indica que no hay ningún cambio en el brillo.</span><span class="sxs-lookup"><span data-stu-id="75d69-116">Zero indicates no change in brightness.</span></span>

## <a name="requirements"></a><span data-ttu-id="75d69-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75d69-117">Requirements</span></span>



| <span data-ttu-id="75d69-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="75d69-118">Requirement</span></span> | <span data-ttu-id="75d69-119">Value</span><span class="sxs-lookup"><span data-stu-id="75d69-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75d69-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75d69-120">Minimum supported client</span></span><br/> | <span data-ttu-id="75d69-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="75d69-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="75d69-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75d69-122">Minimum supported server</span></span><br/> | <span data-ttu-id="75d69-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="75d69-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="75d69-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75d69-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="75d69-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="75d69-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75d69-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="75d69-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d69-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="75d69-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
