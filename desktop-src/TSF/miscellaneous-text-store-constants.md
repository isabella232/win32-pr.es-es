---
title: Constantes de almacén de texto misceláneo (Textstor. h)
description: Las constantes de almacén de texto Miscelánea establecen ciertas propiedades para los almacenes de texto.
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead33c21bb78035dd9fda443a53de575ffa64d9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150859"
---
# <a name="miscellaneous-text-store-constants"></a><span data-ttu-id="b747e-103">Constantes de almacén de texto misceláneo</span><span class="sxs-lookup"><span data-stu-id="b747e-103">Miscellaneous Text Store Constants</span></span>

<span data-ttu-id="b747e-104">Las constantes de almacén de texto Miscelánea establecen ciertas propiedades para los almacenes de texto.</span><span class="sxs-lookup"><span data-stu-id="b747e-104">The miscellaneous text store constants set certain properties for text stores.</span></span>



| <span data-ttu-id="b747e-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="b747e-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="b747e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b747e-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <span data-ttu-id="b747e-107"><dt>**TS \_ \_Selección predeterminada**</dt> <dt>((ulong)-1)</dt></span><span class="sxs-lookup"><span data-stu-id="b747e-107"><dt>**TS\_DEFAULT\_SELECTION**</dt> <dt>( ( ULONG )-1 )</dt></span></span> </dl> | <span data-ttu-id="b747e-108">Si el parámetro *ulIndex* de [ITfContext:: getSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) se establece en este valor, se obtiene la selección predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b747e-108">If the *ulIndex* parameter of [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) is set to this value, the default selection is obtained.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <span data-ttu-id="b747e-109"><dt>**TS \_ GEA \_ oculto**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="b747e-109"><dt>**TS\_GEA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="b747e-110">Si el parámetro *dwFlags* de [ITextStoreAnchor:: GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) se establece en este valor, un objeto incrustado se puede ubicar en el texto oculto.</span><span class="sxs-lookup"><span data-stu-id="b747e-110">If *dwFlags* parameter of [ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) is set to this value, an embedded object can be located within hidden text.</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <span data-ttu-id="b747e-111"><dt>**TS \_ GTA \_ oculto**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="b747e-111"><dt>**TS\_GTA\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="b747e-112">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b747e-112">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <span data-ttu-id="b747e-113"><dt>**TS \_ \_Corrección de St**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="b747e-113"><dt>**TS\_ST\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="b747e-114">Si el parámetro *dwFlags* de [ITextStoreACP:: setText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor:: setText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)o [ITextStoreACPSink:: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) se establece en este valor, el texto es una transformación (corrección) de contenido existente y se conserva cualquier información de marcado de texto especial (metadatos), como datos de archivos. WAV o un identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="b747e-114">If *dwFlags* parameter of [ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext), or [ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <span data-ttu-id="b747e-115"><dt>**TS \_ \_Corrección de TC**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="b747e-115"><dt>**TS\_TC\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                     | <span data-ttu-id="b747e-116">Si el parámetro *dwFlags* de [ITextStoreAnchorSink:: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) se establece en este valor, el texto es una transformación (corrección) de contenido existente y se conserva cualquier información de marcado de texto (metadatos) especial, como datos de archivos. WAV o un identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="b747e-116">If *dwFlags* parameter of [ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) is set to this value, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <span data-ttu-id="b747e-117"><dt>**TS \_ VCOOKIE \_ NUL**</dt> <dt>(0xFFFFFFFF)</dt></span><span class="sxs-lookup"><span data-stu-id="b747e-117"><dt>**TS\_VCOOKIE\_NUL**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                    | <span data-ttu-id="b747e-118">Lo usa internamente TSF.</span><span class="sxs-lookup"><span data-stu-id="b747e-118">Used internally by TSF.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="b747e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b747e-119">Requirements</span></span>



| <span data-ttu-id="b747e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b747e-120">Requirement</span></span> | <span data-ttu-id="b747e-121">Value</span><span class="sxs-lookup"><span data-stu-id="b747e-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b747e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b747e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b747e-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b747e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b747e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b747e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b747e-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b747e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b747e-126">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b747e-126">Redistributable</span></span><br/>          | <span data-ttu-id="b747e-127">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b747e-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="b747e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b747e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b747e-129"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="b747e-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="b747e-130">IDL</span><span class="sxs-lookup"><span data-stu-id="b747e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b747e-131"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b747e-131"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b747e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b747e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b747e-133">ITfContext::GetSelection</span><span class="sxs-lookup"><span data-stu-id="b747e-133">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="b747e-134">ITextStoreACP:: SetText</span><span class="sxs-lookup"><span data-stu-id="b747e-134">ITextStoreACP::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[<span data-ttu-id="b747e-135">ITextStoreAnchor:: SetText</span><span class="sxs-lookup"><span data-stu-id="b747e-135">ITextStoreAnchor::SetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[<span data-ttu-id="b747e-136">ITextStoreAnchor::GetEmbedded</span><span class="sxs-lookup"><span data-stu-id="b747e-136">ITextStoreAnchor::GetEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[<span data-ttu-id="b747e-137">ITextStoreACPSink::OnTextChange</span><span class="sxs-lookup"><span data-stu-id="b747e-137">ITextStoreACPSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="b747e-138">ITextStoreAnchorSink::OnTextChange</span><span class="sxs-lookup"><span data-stu-id="b747e-138">ITextStoreAnchorSink::OnTextChange</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[<span data-ttu-id="b747e-139">Constantes de marco de trabajo variadas</span><span class="sxs-lookup"><span data-stu-id="b747e-139">Miscellaneous Framework Constants</span></span>](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





