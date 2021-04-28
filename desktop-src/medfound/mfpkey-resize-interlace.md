---
description: 'MFPKEY_RESIZE_INTERLACE propiedad : especifica si el flujo de entrada está entrelazado.'
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: MFPKEY_RESIZE_INTERLACE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d0efe93901a08322a05dbed2515f76b04a214b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092883"
---
# <a name="mfpkey_resize_interlace-property"></a><span data-ttu-id="2107c-103">Propiedad MFPKEY \_ RESIZE \_ INTERLACE</span><span class="sxs-lookup"><span data-stu-id="2107c-103">MFPKEY\_RESIZE\_INTERLACE Property</span></span>

<span data-ttu-id="2107c-104">Especifica si el flujo de entrada está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="2107c-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2107c-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2107c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2107c-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="2107c-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2107c-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2107c-107">Data Type</span></span>

<span data-ttu-id="2107c-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="2107c-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="2107c-109">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="2107c-109">Applies To</span></span>

-   [<span data-ttu-id="2107c-110">Video Resizer DSP</span><span class="sxs-lookup"><span data-stu-id="2107c-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="2107c-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2107c-111">Remarks</span></span>

<span data-ttu-id="2107c-112">Utilice uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="2107c-112">Use one of the following values:</span></span>



| <span data-ttu-id="2107c-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2107c-113">Value</span></span>     | <span data-ttu-id="2107c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2107c-114">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="2107c-115">VT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="2107c-115">VT\_FALSE</span></span> | <span data-ttu-id="2107c-116">progresivo</span><span class="sxs-lookup"><span data-stu-id="2107c-116">Progressive</span></span> |
| <span data-ttu-id="2107c-117">VT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="2107c-117">VT\_TRUE</span></span>  | <span data-ttu-id="2107c-118">Interlaced</span><span class="sxs-lookup"><span data-stu-id="2107c-118">Interlaced</span></span>  |



 

<span data-ttu-id="2107c-119">Si no se establece esta propiedad, el DSP usa el tipo de medio de entrada para determinar si el vídeo está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="2107c-119">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="2107c-120">Puede establecer esta propiedad para invalidar la configuración del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="2107c-120">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="2107c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2107c-121">Requirements</span></span>



| <span data-ttu-id="2107c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2107c-122">Requirement</span></span> | <span data-ttu-id="2107c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2107c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2107c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2107c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2107c-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2107c-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2107c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2107c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2107c-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2107c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2107c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2107c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2107c-129"><dt>Wmcodecdsp.h</dt></span><span class="sxs-lookup"><span data-stu-id="2107c-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2107c-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2107c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2107c-131">Media Foundation propiedades</span><span class="sxs-lookup"><span data-stu-id="2107c-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
