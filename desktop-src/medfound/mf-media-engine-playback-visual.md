---
description: Establece un visual DirectComposition de Microsoft como la región de reproducción del motor multimedia.
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: MF_MEDIA_ENGINE_PLAYBACK_VISUAL atributo (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e9c7366bd0fbf4bf36523cf7a68f2d6da70bc3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105649323"
---
# <a name="mf_media_engine_playback_visual-attribute"></a><span data-ttu-id="5b5c1-103">\_ \_ \_ Atributo visual de reproducción del motor multimedia MF \_</span><span class="sxs-lookup"><span data-stu-id="5b5c1-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_VISUAL attribute</span></span>

<span data-ttu-id="5b5c1-104">Establece un visual DirectComposition de Microsoft como la región de reproducción del motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="5b5c1-104">Sets a Microsoft DirectComposition visual as the playback region for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="5b5c1-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5b5c1-105">Data type</span></span>

<span data-ttu-id="5b5c1-106">**IDCompositionVisual \* *_ se almacena como _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="5b5c1-106">**IDCompositionVisual\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="5b5c1-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="5b5c1-107">Get/set</span></span>

<span data-ttu-id="5b5c1-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="5b5c1-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="5b5c1-109">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="5b5c1-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="5b5c1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b5c1-110">Remarks</span></span>

<span data-ttu-id="5b5c1-111">Para obtener más información sobre DirectComposition, vea [DirectComposition](../directcomp/directcomposition-portal.md) y [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).</span><span class="sxs-lookup"><span data-stu-id="5b5c1-111">For more information on DirectComposition, see [DirectComposition](../directcomp/directcomposition-portal.md) and [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).</span></span>

<span data-ttu-id="5b5c1-112">Este atributo se usa con el método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="5b5c1-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b5c1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b5c1-113">Requirements</span></span>



| <span data-ttu-id="5b5c1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b5c1-114">Requirement</span></span> | <span data-ttu-id="5b5c1-115">Value</span><span class="sxs-lookup"><span data-stu-id="5b5c1-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5c1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b5c1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5b5c1-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="5b5c1-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="5b5c1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b5c1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5b5c1-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="5b5c1-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="5b5c1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b5c1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b5c1-121"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b5c1-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b5c1-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b5c1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5c1-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5b5c1-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
