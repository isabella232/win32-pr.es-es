---
description: Especifica el número máximo de pasos admitidos por el codificador.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: Propiedad MFPKEY_PASSESRECOMMENDED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e0a0d254c09965976e5659bacfacf3be06643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276311"
---
# <a name="mfpkey_passesrecommended-property"></a><span data-ttu-id="012f6-103">\_Propiedad PASSESRECOMMENDED de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="012f6-103">MFPKEY\_PASSESRECOMMENDED Property</span></span>

<span data-ttu-id="012f6-104">Especifica el número máximo de pasos admitidos por el codificador.</span><span class="sxs-lookup"><span data-stu-id="012f6-104">Specifies the maximum number of passes supported by the encoder.</span></span> <span data-ttu-id="012f6-105">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="012f6-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="012f6-106">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="012f6-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="012f6-107">g \_ wszWMVCPassesRecommended, g \_ wszWMCPMaxPasses</span><span class="sxs-lookup"><span data-stu-id="012f6-107">g\_wszWMVCPassesRecommended, g\_wszWMCPMaxPasses</span></span>

## <a name="data-type"></a><span data-ttu-id="012f6-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="012f6-108">Data Type</span></span>

<span data-ttu-id="012f6-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="012f6-109">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="012f6-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="012f6-110">Remarks</span></span>

<span data-ttu-id="012f6-111">Puede obtener el valor de esta propiedad llamando a [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span><span class="sxs-lookup"><span data-stu-id="012f6-111">You can get the value of this property calling [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="012f6-112">Si usa **IPropertyBag**, primero debe establecer el valor de FourCC del formato comprimido deseado mediante la propiedad [ \_ FourCC MFPKEY](mfpkey-fourccproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="012f6-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format by using the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="012f6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="012f6-113">Requirements</span></span>



| <span data-ttu-id="012f6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="012f6-114">Requirement</span></span> | <span data-ttu-id="012f6-115">Value</span><span class="sxs-lookup"><span data-stu-id="012f6-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="012f6-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="012f6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="012f6-117">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="012f6-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="012f6-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="012f6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="012f6-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="012f6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="012f6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="012f6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="012f6-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="012f6-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="012f6-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="012f6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="012f6-123">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="012f6-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




