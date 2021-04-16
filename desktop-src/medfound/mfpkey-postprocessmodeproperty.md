---
description: Especifica el modo de procesamiento posterior para el descodificador.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: Propiedad MFPKEY_POSTPROCESSMODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4002deae63f1bdaea09ca31dd95bfec1cb594fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709234"
---
# <a name="mfpkey_postprocessmode-property"></a><span data-ttu-id="9e868-103">\_Propiedad POSTPROCESSMODE de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="9e868-103">MFPKEY\_POSTPROCESSMODE Property</span></span>

<span data-ttu-id="9e868-104">Especifica el modo de procesamiento posterior para el descodificador.</span><span class="sxs-lookup"><span data-stu-id="9e868-104">Specifies the post processing mode for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9e868-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9e868-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9e868-106">**g \_ wszWMVCForcePostProcessMode**</span><span class="sxs-lookup"><span data-stu-id="9e868-106">**g\_wszWMVCForcePostProcessMode**</span></span>

## <a name="data-type"></a><span data-ttu-id="9e868-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9e868-107">Data Type</span></span>

<span data-ttu-id="9e868-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="9e868-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="9e868-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e868-109">Remarks</span></span>

<span data-ttu-id="9e868-110">Establezca esta propiedad en uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="9e868-110">Set this property to one of the following values.</span></span>



| <span data-ttu-id="9e868-111">Value</span><span class="sxs-lookup"><span data-stu-id="9e868-111">Value</span></span> | <span data-ttu-id="9e868-112">Significado</span><span class="sxs-lookup"><span data-stu-id="9e868-112">Meaning</span></span>                                                                                |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e868-113">-1</span><span class="sxs-lookup"><span data-stu-id="9e868-113">-1</span></span>    | <span data-ttu-id="9e868-114">El descodificador establece el modo de procesamiento posterior de forma adaptativa en función de los recursos de CPU disponibles.</span><span class="sxs-lookup"><span data-stu-id="9e868-114">The decoder sets the post processing mode adaptively based on available CPU resources.</span></span> |
| <span data-ttu-id="9e868-115">0</span><span class="sxs-lookup"><span data-stu-id="9e868-115">0</span></span>     | <span data-ttu-id="9e868-116">El descodificador no realiza ningún procesamiento posterior.</span><span class="sxs-lookup"><span data-stu-id="9e868-116">The decoder performs no post processing.</span></span>                                               |
| <span data-ttu-id="9e868-117">1</span><span class="sxs-lookup"><span data-stu-id="9e868-117">1</span></span>     | <span data-ttu-id="9e868-118">el descodificador de la realiza un desbloqueo rápido.</span><span class="sxs-lookup"><span data-stu-id="9e868-118">fThe decoder performs fast deblocking.</span></span>                                                 |
| <span data-ttu-id="9e868-119">2</span><span class="sxs-lookup"><span data-stu-id="9e868-119">2</span></span>     | <span data-ttu-id="9e868-120">El descodificador realiza el desbloqueo completo.</span><span class="sxs-lookup"><span data-stu-id="9e868-120">The decoder performs full deblocking.</span></span>                                                  |
| <span data-ttu-id="9e868-121">3</span><span class="sxs-lookup"><span data-stu-id="9e868-121">3</span></span>     | <span data-ttu-id="9e868-122">El descodificador realiza un desbloqueo y desanillo rápido.</span><span class="sxs-lookup"><span data-stu-id="9e868-122">The decoder performs fast deblocking and deringing.</span></span>                                    |
| <span data-ttu-id="9e868-123">4</span><span class="sxs-lookup"><span data-stu-id="9e868-123">4</span></span>     | <span data-ttu-id="9e868-124">El descodificador realiza el desbloqueo completo y el desanillo.</span><span class="sxs-lookup"><span data-stu-id="9e868-124">The decoder performs full deblocking and deringing.</span></span>                                    |



 

<span data-ttu-id="9e868-125">Como el valor de esta propiedad va de 0 a 4, se incrementa la complejidad de la descodificación, el uso de recursos de CPU y la calidad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="9e868-125">As the value of this property goes from 0 to 4, the decoding complexity, use of CPU resources, and picture quality all increase.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e868-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e868-126">Requirements</span></span>



| <span data-ttu-id="9e868-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e868-127">Requirement</span></span> | <span data-ttu-id="9e868-128">Value</span><span class="sxs-lookup"><span data-stu-id="9e868-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e868-129">Remoto</span><span class="sxs-lookup"><span data-stu-id="9e868-129">Client</span></span><br/> | <span data-ttu-id="9e868-130">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="9e868-130">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="9e868-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e868-131">Header</span></span><br/> | <dl> <span data-ttu-id="9e868-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e868-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e868-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e868-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e868-134">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e868-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




