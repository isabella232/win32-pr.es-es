---
description: Especifica una representación numérica del equilibrio entre la suavidad de movimiento y la calidad de la imagen de la salida del códec.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: Propiedad MFPKEY_CRISP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812764"
---
# <a name="mfpkey_crisp-property"></a><span data-ttu-id="30b5e-103">MFPKEY \_ propiedad nítida</span><span class="sxs-lookup"><span data-stu-id="30b5e-103">MFPKEY\_CRISP Property</span></span>

<span data-ttu-id="30b5e-104">Especifica una representación numérica del equilibrio entre la suavidad de movimiento y la calidad de la imagen de la salida del códec.</span><span class="sxs-lookup"><span data-stu-id="30b5e-104">Specifies a numeric representation of the tradeoff between motion smoothness and image quality of codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="30b5e-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="30b5e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="30b5e-106">g \_ wszWMVCCrisp</span><span class="sxs-lookup"><span data-stu-id="30b5e-106">g\_wszWMVCCrisp</span></span>

## <a name="data-type"></a><span data-ttu-id="30b5e-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="30b5e-107">Data Type</span></span>

<span data-ttu-id="30b5e-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="30b5e-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="30b5e-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="30b5e-109">Default Value</span></span>

<span data-ttu-id="30b5e-110">75</span><span class="sxs-lookup"><span data-stu-id="30b5e-110">75</span></span>

## <a name="remarks"></a><span data-ttu-id="30b5e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30b5e-111">Remarks</span></span>

<span data-ttu-id="30b5e-112">Este valor entero puede oscilar entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="30b5e-112">This integer value can range from 0 to 100.</span></span> <span data-ttu-id="30b5e-113">Cuanto mayor sea el valor, más el códec optimizará la codificación para la calidad de la imagen de los fotogramas individuales, lo que normalmente reduce la suavidad del movimiento.</span><span class="sxs-lookup"><span data-stu-id="30b5e-113">The higher the value, the more the codec will optimize encoding for the image quality of individual frames, which usually reduces motion smoothness.</span></span>

<span data-ttu-id="30b5e-114">Esta propiedad solo debe establecerse para la codificación de velocidad de bits constante (CBR).</span><span class="sxs-lookup"><span data-stu-id="30b5e-114">This property should be set only for constant-bit-rate (CBR) encoding.</span></span> <span data-ttu-id="30b5e-115">Las optimizaciones de la codificación de velocidad de bits variable (VBR) funcionan de manera diferente.</span><span class="sxs-lookup"><span data-stu-id="30b5e-115">The optimizations for variable-bit-rate (VBR) encoding work differently.</span></span>

## <a name="requirements"></a><span data-ttu-id="30b5e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30b5e-116">Requirements</span></span>



| <span data-ttu-id="30b5e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="30b5e-117">Requirement</span></span> | <span data-ttu-id="30b5e-118">Value</span><span class="sxs-lookup"><span data-stu-id="30b5e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30b5e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30b5e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="30b5e-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="30b5e-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="30b5e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30b5e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="30b5e-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="30b5e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30b5e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30b5e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="30b5e-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="30b5e-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30b5e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="30b5e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b5e-126">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="30b5e-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




