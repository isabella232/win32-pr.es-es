---
description: Especifica si el origen de medios ASF utiliza búsquedas aproximadas.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: Propiedad MFPKEY_ASFMediaSource_ApproxSeek (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253a18ebbdf78e3aa0ef0e79f41c4bf180a04b48
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697972"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a><span data-ttu-id="64954-103">\_ \_ Propiedad APPROXSEEK de MFPKEY ASFMediaSource</span><span class="sxs-lookup"><span data-stu-id="64954-103">MFPKEY\_ASFMediaSource\_ApproxSeek property</span></span>

<span data-ttu-id="64954-104">Especifica si el origen de medios ASF utiliza búsquedas aproximadas.</span><span class="sxs-lookup"><span data-stu-id="64954-104">Specifies whether the ASF media source uses approximate seeking.</span></span>



<span data-ttu-id="64954-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="64954-105">Data type</span></span>

<span data-ttu-id="64954-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="64954-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="64954-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="64954-107">PROPVARIANT member</span></span>

<span data-ttu-id="64954-108">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="64954-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="64954-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="64954-109">VT\_BOOL</span></span>

<span data-ttu-id="64954-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="64954-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="64954-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64954-111">Remarks</span></span>

<span data-ttu-id="64954-112">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de medios ASF.</span><span class="sxs-lookup"><span data-stu-id="64954-112">Applications can use this property to configure the ASF media source.</span></span> <span data-ttu-id="64954-113">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="64954-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="64954-114">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="64954-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="64954-115">El origen de medios ASF controla la búsqueda de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="64954-115">The ASF media source handles seeking as follows:</span></span>

-   <span data-ttu-id="64954-116">Si el valor de esta propiedad es **Variant \_ true**, el origen multimedia utiliza una búsqueda aproximada, que es menos precisa pero más rápida que la búsqueda exacta.</span><span class="sxs-lookup"><span data-stu-id="64954-116">If the value of this property is **VARIANT\_TRUE**, the media source uses approximate seeking, which is less accurate but faster than exact seeking.</span></span>
-   <span data-ttu-id="64954-117">Si el valor es **Variant \_ false** y el archivo ASF tiene un índice, el origen multimedia utiliza una búsqueda exacta.</span><span class="sxs-lookup"><span data-stu-id="64954-117">If the value is **VARIANT\_FALSE** and the ASF file has an index, the media source uses exact seeking.</span></span>
-   <span data-ttu-id="64954-118">Si el archivo ASF no contiene un índice, el origen del medio usa la búsqueda de approxmate a menos que la propiedad [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) esté establecida en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="64954-118">If the ASF file does not contain an index, the media source uses approxmate seeking unless the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is set to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="64954-119">Si el archivo ASF no contiene un índice y la propiedad [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) es **Variant \_ true**, el origen multimedia utiliza búsquedas iterativas.</span><span class="sxs-lookup"><span data-stu-id="64954-119">If the ASF file does not contain an index and the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is **VARIANT\_TRUE**, the media source uses iterative seeking.</span></span> <span data-ttu-id="64954-120">La búsqueda iterativa es más precisa pero más lenta que la búsqueda aproximada (pero generalmente menos precisa que la búsqueda exacta).</span><span class="sxs-lookup"><span data-stu-id="64954-120">Iterative seeking is more accurate but slower than approximate seeking (but generally less accurate than exact seeking).</span></span>
    > [!Note]  
    > <span data-ttu-id="64954-121">Requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="64954-121">Requires Windows 7.</span></span>

     

<span data-ttu-id="64954-122">El valor predeterminado de esta propiedad es **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="64954-122">The default value of this property is **VARIANT\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="64954-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64954-123">Requirements</span></span>



| <span data-ttu-id="64954-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="64954-124">Requirement</span></span> | <span data-ttu-id="64954-125">Value</span><span class="sxs-lookup"><span data-stu-id="64954-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64954-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64954-126">Minimum supported client</span></span><br/> | <span data-ttu-id="64954-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="64954-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="64954-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64954-128">Minimum supported server</span></span><br/> | <span data-ttu-id="64954-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="64954-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="64954-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64954-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="64954-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="64954-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64954-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="64954-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64954-133">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="64954-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




