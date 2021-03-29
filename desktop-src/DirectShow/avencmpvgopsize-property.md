---
description: Especifica el número máximo de imágenes de un encabezado de grupo de imágenes (GOP) al siguiente encabezado GOP.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: Propiedad AVEncMPVGOPSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8907d0992153039b1af9a9a0e82ee5782b525d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080030"
---
# <a name="avencmpvgopsize-property"></a><span data-ttu-id="8e919-103">Propiedad AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="8e919-103">AVEncMPVGOPSize property</span></span>

<span data-ttu-id="8e919-104">Especifica el número máximo de imágenes de un encabezado de grupo de imágenes (GOP) al siguiente encabezado GOP.</span><span class="sxs-lookup"><span data-stu-id="8e919-104">Specifies the maximum number of pictures from one group-of-pictures (GOP) header to the next GOP header.</span></span>

<span data-ttu-id="8e919-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8e919-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="8e919-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8e919-106">Data type</span></span>

<span data-ttu-id="8e919-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="8e919-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8e919-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="8e919-108">Property GUID</span></span>

<span data-ttu-id="8e919-109">**CODECAPI \_ AVEncMPVGOPSize**</span><span class="sxs-lookup"><span data-stu-id="8e919-109">**CODECAPI\_AVEncMPVGOPSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="8e919-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8e919-110">Property value</span></span>

<span data-ttu-id="8e919-111">Los codificadores pueden implementar esta propiedad como un conjunto enumerado o como un intervalo lineal.</span><span class="sxs-lookup"><span data-stu-id="8e919-111">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e919-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e919-112">Remarks</span></span>

<span data-ttu-id="8e919-113">Establezca esta propiedad antes de iniciar una grabación.</span><span class="sxs-lookup"><span data-stu-id="8e919-113">Set this property before starting a recording.</span></span>

<span data-ttu-id="8e919-114">**Se aplica a Windows 8:** El tamaño de GOP codificado debe ser menor o igual que el número especificado a través de esta propiedad, para mantener el mismo patrón de marco B establecido por [CODECAPI \_ AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) en el GOP o debido al cambio de la escena.</span><span class="sxs-lookup"><span data-stu-id="8e919-114">**Applies to Windows 8:** The encoded GOP size shall be smaller than or equal to the specified number through this property, in order to keep the same B frame pattern set by [CODECAPI\_AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) throughout the GOP or due to scene change.</span></span> <span data-ttu-id="8e919-115">Por ejemplo, cuando el número de fotogramas B de un GOP se especifica en 2, y el tamaño del GOP es 11, el codificador producirá un tamaño GOP de 10 fotogramas o menos.</span><span class="sxs-lookup"><span data-stu-id="8e919-115">For example, when the number of B frames in a GOP is specified to be 2, and GOP size is 11, then encoder shall produce GOP size of 10 frames or less.</span></span> <span data-ttu-id="8e919-116">Cuando se produce un cambio de escena en medio de un GOP, el codificador también podría insertar el fotograma clave y producir un GOP más pequeño.</span><span class="sxs-lookup"><span data-stu-id="8e919-116">When scene change happens in the middle of a GOP, encoder might also insert key frame and produce smaller GOP.</span></span>

<span data-ttu-id="8e919-117">El tamaño de GOP 0 es dependiente del codificador y los codificadores pueden elegir diferentes tamaños de GOP en función de su implementación, calidad y rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8e919-117">GOP size 0 is encoder dependent and encoders can choose different GOP sizes based on their implementation/quality/performance.</span></span> <span data-ttu-id="8e919-118">Los codificadores deben respetar el tamaño del GOP y truncar los fotogramas B en este caso.</span><span class="sxs-lookup"><span data-stu-id="8e919-118">Encoders should honor the GOP size and truncate B frames in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e919-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e919-119">Requirements</span></span>



| <span data-ttu-id="8e919-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e919-120">Requirement</span></span> | <span data-ttu-id="8e919-121">Value</span><span class="sxs-lookup"><span data-stu-id="8e919-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e919-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e919-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e919-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="8e919-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8e919-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e919-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e919-125">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="8e919-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8e919-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e919-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e919-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e919-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e919-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e919-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e919-129">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="8e919-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="8e919-130">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="8e919-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




