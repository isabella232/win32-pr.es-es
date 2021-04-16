---
description: Ajusta el contraste.
ms.assetid: 32ae514a-eeba-4205-b6e6-70fc01b93a95
title: Propiedad MFPKEY_COLOR_CONTRAST (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5de0733e743c3ce12bfe9a04159a2e881bf2143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715881"
---
# <a name="mfpkey_color_contrast-property"></a><span data-ttu-id="f129d-103">\_Propiedad contraste de color MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="f129d-103">MFPKEY\_COLOR\_CONTRAST Property</span></span>

<span data-ttu-id="f129d-104">Ajusta el contraste.</span><span class="sxs-lookup"><span data-stu-id="f129d-104">Adjusts the contrast.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f129d-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f129d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f129d-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="f129d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f129d-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f129d-107">Data Type</span></span>

<span data-ttu-id="f129d-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f129d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="f129d-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f129d-109">Default Value</span></span>

<span data-ttu-id="f129d-110">0</span><span class="sxs-lookup"><span data-stu-id="f129d-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="f129d-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="f129d-111">Applies To</span></span>

-   [<span data-ttu-id="f129d-112">DSP de transformación de control de color</span><span class="sxs-lookup"><span data-stu-id="f129d-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="f129d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f129d-113">Remarks</span></span>

<span data-ttu-id="f129d-114">El ajuste de contraste se realiza multiplicando los valores de YCbCr por un factor de escala.</span><span class="sxs-lookup"><span data-stu-id="f129d-114">Contrast adjustment is performed by multiplying the YCbCr values by a scaling factor.</span></span>

<span data-ttu-id="f129d-115">Esta propiedad tiene un intervalo de-127 a 127.</span><span class="sxs-lookup"><span data-stu-id="f129d-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="f129d-116">Cero indica que no hay ningún cambio en contraste.</span><span class="sxs-lookup"><span data-stu-id="f129d-116">Zero indicates no change in contrast.</span></span>

## <a name="requirements"></a><span data-ttu-id="f129d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f129d-117">Requirements</span></span>



| <span data-ttu-id="f129d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f129d-118">Requirement</span></span> | <span data-ttu-id="f129d-119">Value</span><span class="sxs-lookup"><span data-stu-id="f129d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f129d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f129d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f129d-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f129d-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f129d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f129d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f129d-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f129d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f129d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f129d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f129d-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f129d-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f129d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f129d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f129d-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f129d-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
