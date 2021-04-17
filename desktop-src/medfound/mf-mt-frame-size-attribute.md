---
description: Ancho y alto de un fotograma de vídeo, en píxeles.
ms.assetid: 9f10a972-406f-47ef-b71c-86ed771c9a9a
title: MF_MT_FRAME_SIZE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3d6278cdbd4c279c498839cb183b3331fe1efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659983"
---
# <a name="mf_mt_frame_size-attribute"></a><span data-ttu-id="59d08-103">\_Atributo de \_ tamaño de marco MF MT \_</span><span class="sxs-lookup"><span data-stu-id="59d08-103">MF\_MT\_FRAME\_SIZE attribute</span></span>

<span data-ttu-id="59d08-104">Ancho y alto de un fotograma de vídeo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="59d08-104">Width and height of a video frame, in pixels.</span></span>

## <a name="data-type"></a><span data-ttu-id="59d08-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="59d08-105">Data type</span></span>

<span data-ttu-id="59d08-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="59d08-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="59d08-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59d08-107">Remarks</span></span>

<span data-ttu-id="59d08-108">Los 32 bits superiores contienen el ancho y los bits inferiores 32 contienen el alto.</span><span class="sxs-lookup"><span data-stu-id="59d08-108">The upper 32 bits contain the width and the lower 32 bits contain the height.</span></span>

<span data-ttu-id="59d08-109">Para establecer este atributo, utilice la función [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) .</span><span class="sxs-lookup"><span data-stu-id="59d08-109">To set this attribute, use the [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) function.</span></span> <span data-ttu-id="59d08-110">Para obtener este atributo, utilice la función [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) .</span><span class="sxs-lookup"><span data-stu-id="59d08-110">To get this attribute, use the [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) function.</span></span>

<span data-ttu-id="59d08-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="59d08-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="59d08-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="59d08-112">Examples</span></span>


```
// Helper function to set the frame size on a video media type.
inline HRESULT SetFrameSize(IMFMediaType *pType, UINT32 width, UINT32 height)
{
    return MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
}

// Helper function to get the frame size from a video media type.
inline HRESULT GetFrameSize(IMFMediaType *pType, UINT32 *pWidth, UINT32 *pHeight)
{
    return MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, pWidth, pHeight);
}
```



## <a name="requirements"></a><span data-ttu-id="59d08-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59d08-113">Requirements</span></span>



| <span data-ttu-id="59d08-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="59d08-114">Requirement</span></span> | <span data-ttu-id="59d08-115">Value</span><span class="sxs-lookup"><span data-stu-id="59d08-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59d08-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59d08-116">Minimum supported client</span></span><br/> | <span data-ttu-id="59d08-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="59d08-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="59d08-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59d08-118">Minimum supported server</span></span><br/> | <span data-ttu-id="59d08-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="59d08-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="59d08-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59d08-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="59d08-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="59d08-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59d08-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="59d08-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59d08-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59d08-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="59d08-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="59d08-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="59d08-125">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="59d08-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




