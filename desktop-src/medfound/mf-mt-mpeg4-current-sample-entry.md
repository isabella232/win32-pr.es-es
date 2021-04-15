---
description: Especifica la entrada actual en el cuadro Descripción del ejemplo para un tipo de medio MPEG-4.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648517"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a><span data-ttu-id="7577a-103">\_Atributo de \_ entrada de ejemplo de MPEG4 \_ actual \_ \_ de MF MT</span><span class="sxs-lookup"><span data-stu-id="7577a-103">MF\_MT\_MPEG4\_CURRENT\_SAMPLE\_ENTRY attribute</span></span>

<span data-ttu-id="7577a-104">Especifica la entrada actual en el cuadro Descripción del ejemplo para un tipo de medio MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="7577a-104">Specifies the current entry in the sample description box for an MPEG-4 media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="7577a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7577a-105">Data type</span></span>

<span data-ttu-id="7577a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7577a-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7577a-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="7577a-107">Get/set</span></span>

<span data-ttu-id="7577a-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7577a-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7577a-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7577a-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="7577a-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="7577a-110">Applies to</span></span>

[<span data-ttu-id="7577a-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="7577a-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="7577a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7577a-112">Remarks</span></span>

<span data-ttu-id="7577a-113">En un archivo MP4 o 3GP, el cuadro Descripción del ejemplo describe la codificación utilizada para una secuencia en el archivo.</span><span class="sxs-lookup"><span data-stu-id="7577a-113">In an MP4 or 3GP file, the sample description box describes the encoding used for a stream in the file.</span></span> <span data-ttu-id="7577a-114">El cuadro Descripción del ejemplo puede contener varias entradas.</span><span class="sxs-lookup"><span data-stu-id="7577a-114">The sample description box can contain multiple entries.</span></span> <span data-ttu-id="7577a-115">Este atributo especifica la entrada que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="7577a-115">This attribute specifies which entry to use.</span></span> <span data-ttu-id="7577a-116">El valor es un índice basado en cero en la lista.</span><span class="sxs-lookup"><span data-stu-id="7577a-116">The value is a zero-based index into the list.</span></span>

<span data-ttu-id="7577a-117">Actualmente, el único valor admitido es 0.</span><span class="sxs-lookup"><span data-stu-id="7577a-117">Currently, the only supported value is 0.</span></span> <span data-ttu-id="7577a-118">El atributo se ha definido para la extensibilidad futura.</span><span class="sxs-lookup"><span data-stu-id="7577a-118">The attribute has been defined for future extensibility.</span></span>

<span data-ttu-id="7577a-119">El origen de archivo MPEG-4 siempre establece el valor en 0.</span><span class="sxs-lookup"><span data-stu-id="7577a-119">The MPEG-4 file source always sets the value to 0.</span></span> <span data-ttu-id="7577a-120">Los receptores de archivos MP4 y 3GP omiten el valor de este atributo si está presente.</span><span class="sxs-lookup"><span data-stu-id="7577a-120">The MP4 and 3GP file sinks ignore the value of this attribute if it is present.</span></span>

<span data-ttu-id="7577a-121">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7577a-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7577a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7577a-122">Requirements</span></span>



| <span data-ttu-id="7577a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7577a-123">Requirement</span></span> | <span data-ttu-id="7577a-124">Value</span><span class="sxs-lookup"><span data-stu-id="7577a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7577a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7577a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7577a-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="7577a-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="7577a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7577a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7577a-128">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="7577a-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7577a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7577a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7577a-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7577a-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7577a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7577a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7577a-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7577a-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7577a-133">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="7577a-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="7577a-134">\_Descripción del \_ ejemplo de MPEG4 MT \_ de MF \_</span><span class="sxs-lookup"><span data-stu-id="7577a-134">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION</span></span>](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




