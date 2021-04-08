---
description: Especifica el FOURCC que identifica el codificador que se desea utilizar.
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: Propiedad MFPKEY_FOURCC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001632"
---
# <a name="mfpkey_fourcc-property"></a><span data-ttu-id="a34e1-103">MFPKEY \_ FourCC (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a34e1-103">MFPKEY\_FOURCC Property</span></span>

<span data-ttu-id="a34e1-104">Especifica el FOURCC que identifica el codificador que se desea utilizar.</span><span class="sxs-lookup"><span data-stu-id="a34e1-104">Specifies the FOURCC that identifies the encoder you want to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a34e1-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a34e1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a34e1-106">g \_ wszWMVCFOURCC</span><span class="sxs-lookup"><span data-stu-id="a34e1-106">g\_wszWMVCFOURCC</span></span>

## <a name="data-type"></a><span data-ttu-id="a34e1-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a34e1-107">Data Type</span></span>

<span data-ttu-id="a34e1-108">VT \_ I4 (valor FourCC)</span><span class="sxs-lookup"><span data-stu-id="a34e1-108">VT\_I4 (FOURCC value)</span></span>

## <a name="remarks"></a><span data-ttu-id="a34e1-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a34e1-109">Remarks</span></span>

<span data-ttu-id="a34e1-110">Debe establecer este valor antes de recuperar los valores de las siguientes propiedades mediante **IPropertyBag** o **IPropertyStore**:</span><span class="sxs-lookup"><span data-stu-id="a34e1-110">You must set this value before retrieving the values for the following properties using **IPropertyBag** or **IPropertyStore**:</span></span>

-   [<span data-ttu-id="a34e1-111">MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE</span><span class="sxs-lookup"><span data-stu-id="a34e1-111">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE</span></span>](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [<span data-ttu-id="a34e1-112">MFPKEY \_ PASSESRECOMMENDED</span><span class="sxs-lookup"><span data-stu-id="a34e1-112">MFPKEY\_PASSESRECOMMENDED</span></span>](mfpkey-passesrecommendedproperty.md)

<span data-ttu-id="a34e1-113">Debe usar [**IWMCodecProps:: GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) para recuperar los valores de las propiedades dependientes de FourCC mencionadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a34e1-113">You should use [**IWMCodecProps::GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) to retrieve the values of the FOURCC-dependent properties listed previously.</span></span> <span data-ttu-id="a34e1-114">Cuando se usa **GetCodecProp**, no es necesario establecer **MFPKEY \_ FourCC**.</span><span class="sxs-lookup"><span data-stu-id="a34e1-114">When using **GetCodecProp**, you do not need to set **MFPKEY\_FOURCC**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a34e1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a34e1-115">Requirements</span></span>



| <span data-ttu-id="a34e1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a34e1-116">Requirement</span></span> | <span data-ttu-id="a34e1-117">Value</span><span class="sxs-lookup"><span data-stu-id="a34e1-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a34e1-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a34e1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a34e1-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a34e1-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a34e1-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a34e1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a34e1-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a34e1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a34e1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a34e1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a34e1-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a34e1-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a34e1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a34e1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a34e1-125">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a34e1-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




