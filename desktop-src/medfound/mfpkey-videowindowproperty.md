---
description: Especifica la cantidad de contenido, en milisegundos, que puede caber en el búfer del modelo.
ms.assetid: da959bef-1e87-4638-9a77-4135c31a3d27
title: Propiedad MFPKEY_VIDEOWINDOW (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33d10b3a589ef3bcfc945b2c3404c7b02cb7121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543979"
---
# <a name="mfpkey_videowindow-property"></a><span data-ttu-id="b0b6e-103">MFPKEY \_ (propiedad de VideoWindow)</span><span class="sxs-lookup"><span data-stu-id="b0b6e-103">MFPKEY\_VIDEOWINDOW Property</span></span>

<span data-ttu-id="b0b6e-104">Especifica la cantidad de contenido, en milisegundos, que puede caber en el búfer del modelo.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-104">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b0b6e-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b0b6e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b0b6e-106">g \_ wszWMVCVideoWIndow</span><span class="sxs-lookup"><span data-stu-id="b0b6e-106">g\_wszWMVCVideoWIndow</span></span>

## <a name="data-type"></a><span data-ttu-id="b0b6e-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b0b6e-107">Data Type</span></span>

<span data-ttu-id="b0b6e-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b0b6e-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="b0b6e-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b0b6e-109">Default Value</span></span>

<span data-ttu-id="b0b6e-110">3000</span><span class="sxs-lookup"><span data-stu-id="b0b6e-110">3000</span></span>

## <a name="remarks"></a><span data-ttu-id="b0b6e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0b6e-111">Remarks</span></span>

<span data-ttu-id="b0b6e-112">La ventana de búfer es uno de los parámetros del modelo de "depósito de fugas" que se usa en el control de velocidad de códec.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-112">The buffer window is one of the "leaky bucket" model parameters used in the codec rate control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b6e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0b6e-113">Requirements</span></span>



| <span data-ttu-id="b0b6e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0b6e-114">Requirement</span></span> | <span data-ttu-id="b0b6e-115">Value</span><span class="sxs-lookup"><span data-stu-id="b0b6e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b6e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0b6e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b6e-117">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b0b6e-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b0b6e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0b6e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b6e-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0b6e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b0b6e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0b6e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0b6e-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0b6e-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0b6e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0b6e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b6e-123">Configuración de la codificación de vídeo</span><span class="sxs-lookup"><span data-stu-id="b0b6e-123">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="b0b6e-124">El modelo de búfer de depósito con fugas</span><span class="sxs-lookup"><span data-stu-id="b0b6e-124">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="b0b6e-125">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b0b6e-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




