---
description: Especifica si el flujo de entrada está entrelazado.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: Propiedad MFPKEY_RESIZE_INTERLACE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a27504bd6da92bc48fee04afc999568a514fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666921"
---
# <a name="mfpkey_resize_interlace-property"></a><span data-ttu-id="f913b-103">MFPKEY \_ cambiar el tamaño de la \_ propiedad entrelazada</span><span class="sxs-lookup"><span data-stu-id="f913b-103">MFPKEY\_RESIZE\_INTERLACE Property</span></span>

<span data-ttu-id="f913b-104">Especifica si el flujo de entrada está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="f913b-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f913b-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f913b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f913b-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="f913b-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f913b-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f913b-107">Data Type</span></span>

<span data-ttu-id="f913b-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="f913b-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="f913b-109">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="f913b-109">Applies To</span></span>

-   [<span data-ttu-id="f913b-110">Vídeo de tamaño DSP</span><span class="sxs-lookup"><span data-stu-id="f913b-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="f913b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f913b-111">Remarks</span></span>

<span data-ttu-id="f913b-112">Utilice uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="f913b-112">Use one of the following values:</span></span>



| <span data-ttu-id="f913b-113">Value</span><span class="sxs-lookup"><span data-stu-id="f913b-113">Value</span></span>     | <span data-ttu-id="f913b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f913b-114">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="f913b-115">VT \_ falso</span><span class="sxs-lookup"><span data-stu-id="f913b-115">VT\_FALSE</span></span> | <span data-ttu-id="f913b-116">progresivo</span><span class="sxs-lookup"><span data-stu-id="f913b-116">Progressive</span></span> |
| <span data-ttu-id="f913b-117">VT \_ true</span><span class="sxs-lookup"><span data-stu-id="f913b-117">VT\_TRUE</span></span>  | <span data-ttu-id="f913b-118">Interlaced</span><span class="sxs-lookup"><span data-stu-id="f913b-118">Interlaced</span></span>  |



 

<span data-ttu-id="f913b-119">Si no se establece esta propiedad, el DSP usa el tipo de medio de entrada para determinar si el vídeo está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="f913b-119">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="f913b-120">Puede establecer esta propiedad para invalidar la configuración de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="f913b-120">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="f913b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f913b-121">Requirements</span></span>



| <span data-ttu-id="f913b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f913b-122">Requirement</span></span> | <span data-ttu-id="f913b-123">Value</span><span class="sxs-lookup"><span data-stu-id="f913b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f913b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f913b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f913b-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f913b-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f913b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f913b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f913b-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f913b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f913b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f913b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f913b-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f913b-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f913b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f913b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f913b-131">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f913b-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
