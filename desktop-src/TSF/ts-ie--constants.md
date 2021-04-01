---
title: Constantes de TS_IE_ (Textstor. h)
description: Las constantes de TS \_ IE \_ \ describen cómo insertar texto que puede contener objetos incrustados utilizados por servicios de texto.
ms.assetid: a455d712-42d5-472e-862d-85ae3ba9149f
topic_type:
- apiref
api_name:
- TS_IE_CORRECTION
- TS_IE_COMPOSITION
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9abdb05ba065ed9bf41b5379060c0643053884e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150094"
---
# <a name="ts_ie_-constants"></a><span data-ttu-id="56475-103">\_Constantes de IE de TS \_ \*</span><span class="sxs-lookup"><span data-stu-id="56475-103">TS\_IE\_\* Constants</span></span>

<span data-ttu-id="56475-104">Las constantes de IE de TS \_ \_ \* describen cómo insertar texto que puede contener objetos incrustados utilizados por servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="56475-104">The TS\_IE\_\* constants describe how to insert text that can contain embedded objects used by text services.</span></span>



| <span data-ttu-id="56475-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="56475-105">Constant/value</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="56475-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="56475-106">Description</span></span>                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IE_CORRECTION"></span><span id="ts_ie_correction"></span><dl> <span data-ttu-id="56475-107"><dt>**TS \_ \_Corrección de IE**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="56475-107"><dt>**TS\_IE\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>    | <span data-ttu-id="56475-108">El texto es una transformación (corrección) de contenido existente y se conserva cualquier información de marcado de texto (metadatos) especial, como datos de archivos. WAV o un identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="56475-108">The text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_IE_COMPOSITION"></span><span id="ts_ie_composition"></span><dl> <span data-ttu-id="56475-109"><dt>**TS \_ \_Composición de IE**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="56475-109"><dt>**TS\_IE\_COMPOSITION**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="56475-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="56475-110">Not used.</span></span><br/>                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="56475-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56475-111">Remarks</span></span>

<span data-ttu-id="56475-112">Estas constantes se utilizan en el parámetro *dwFlags* de [ITextStoreACP:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) y [ITextStoreAnchor:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).</span><span class="sxs-lookup"><span data-stu-id="56475-112">These constants are used in the *dwFlags* parameter of [ITextStoreACP::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) and [ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).</span></span>

## <a name="requirements"></a><span data-ttu-id="56475-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56475-113">Requirements</span></span>



| <span data-ttu-id="56475-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="56475-114">Requirement</span></span> | <span data-ttu-id="56475-115">Value</span><span class="sxs-lookup"><span data-stu-id="56475-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56475-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56475-116">Minimum supported client</span></span><br/> | <span data-ttu-id="56475-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="56475-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="56475-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56475-118">Minimum supported server</span></span><br/> | <span data-ttu-id="56475-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="56475-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56475-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="56475-120">Redistributable</span></span><br/>          | <span data-ttu-id="56475-121">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="56475-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="56475-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56475-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="56475-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="56475-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="56475-124">IDL</span><span class="sxs-lookup"><span data-stu-id="56475-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56475-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56475-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56475-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="56475-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56475-127">ITextStoreACP:: InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="56475-127">ITextStoreACP::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> <dt>

[<span data-ttu-id="56475-128">ITextStoreAnchor::InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="56475-128">ITextStoreAnchor::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)
</dt> </dl>

 

 





