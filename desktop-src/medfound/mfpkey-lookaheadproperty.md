---
description: Especifica el número de fotogramas después del fotograma actual que el códec evaluará antes de codificar el fotograma actual.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: Propiedad MFPKEY_LOOKAHEAD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a024c4d0be6ef7ab16c4bf51f290b01de3282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696943"
---
# <a name="mfpkey_lookahead-property"></a><span data-ttu-id="293fd-103">\_Propiedad de búsqueda anticipada MFPKEY</span><span class="sxs-lookup"><span data-stu-id="293fd-103">MFPKEY\_LOOKAHEAD Property</span></span>

<span data-ttu-id="293fd-104">Especifica el número de fotogramas después del fotograma actual que el códec evaluará antes de codificar el fotograma actual.</span><span class="sxs-lookup"><span data-stu-id="293fd-104">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="293fd-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="293fd-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="293fd-106">g \_ wszWMVCLookAhead</span><span class="sxs-lookup"><span data-stu-id="293fd-106">g\_wszWMVCLookAhead</span></span>

## <a name="data-type"></a><span data-ttu-id="293fd-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="293fd-107">Data Type</span></span>

<span data-ttu-id="293fd-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="293fd-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="293fd-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="293fd-109">Default Value</span></span>

<span data-ttu-id="293fd-110">0</span><span class="sxs-lookup"><span data-stu-id="293fd-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="293fd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="293fd-111">Remarks</span></span>

<span data-ttu-id="293fd-112">Cuando el códec usa la búsqueda anticipada, puede codificar el vídeo de forma más eficaz.</span><span class="sxs-lookup"><span data-stu-id="293fd-112">When the codec uses lookahead, it can encode the video more efficiently.</span></span>

<span data-ttu-id="293fd-113">El objeto de escritor del SDK de Windows Media Format espera que el códec codifique cada ejemplo inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="293fd-113">The writer object of the Windows Media Format SDK expects the codec to encode each sample immediately.</span></span> <span data-ttu-id="293fd-114">Como resultado, esta característica no funciona correctamente en el software que utiliza el objeto de escritor (incluido Windows Media Encoder y Windows Media Player).</span><span class="sxs-lookup"><span data-stu-id="293fd-114">As a result, this feature does not work properly in software that uses the writer object (including Windows Media Encoder and Windows Media Player).</span></span> <span data-ttu-id="293fd-115">Cualquier extensión de unidad de datos asociada con fotogramas de vídeo se adjuntará al fotograma de salida incorrecto.</span><span class="sxs-lookup"><span data-stu-id="293fd-115">Any data unit extensions associated with video frames will be attached to the wrong output frame.</span></span> <span data-ttu-id="293fd-116">El número de fotogramas por los que las extensiones de unidad de datos se colocan de forma no es igual al número de fotogramas de la búsqueda anticipada que se usan.</span><span class="sxs-lookup"><span data-stu-id="293fd-116">The number of frames by which the data unit extensions are misplaced is equal to the number of frames of lookahead that are used.</span></span>

<span data-ttu-id="293fd-117">Los valores de búsqueda anticipada válidos van de 0 a 16 fotogramas.</span><span class="sxs-lookup"><span data-stu-id="293fd-117">Valid lookahead values range from 0 to 16 frames.</span></span> <span data-ttu-id="293fd-118">El valor recomendado es 16.</span><span class="sxs-lookup"><span data-stu-id="293fd-118">The recommended value is 16.</span></span>

## <a name="requirements"></a><span data-ttu-id="293fd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="293fd-119">Requirements</span></span>



| <span data-ttu-id="293fd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="293fd-120">Requirement</span></span> | <span data-ttu-id="293fd-121">Value</span><span class="sxs-lookup"><span data-stu-id="293fd-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="293fd-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="293fd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="293fd-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="293fd-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="293fd-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="293fd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="293fd-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="293fd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="293fd-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="293fd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="293fd-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="293fd-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="293fd-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="293fd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="293fd-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="293fd-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




