---
title: ID2D1RenderTarget métodos DrawText
description: Dibuja el texto especificado utilizando la información de formato proporcionada por un objeto IDWriteTextFormat.
ms.assetid: 7cda7854-f9df-48d3-bc62-6aaee769e6f9
keywords:
- Métodos DrawText Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5ace5c64dc90f057ff9fdfe5a79d664137c38030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679221"
---
# <a name="id2d1rendertargetdrawtext-methods"></a><span data-ttu-id="233ae-104">ID2D1RenderTarget::D rawText métodos)</span><span class="sxs-lookup"><span data-stu-id="233ae-104">ID2D1RenderTarget::DrawText methods</span></span>

<span data-ttu-id="233ae-105">Dibuja el texto especificado utilizando la información de formato proporcionada por un objeto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="233ae-105">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="233ae-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="233ae-106">Overload list</span></span>



| <span data-ttu-id="233ae-107">Método</span><span class="sxs-lookup"><span data-stu-id="233ae-107">Method</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="233ae-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="233ae-108">Description</span></span>                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="233ae-109">[**DrawText (WCHAR \* , IDWriteTextFormat \* , D2D1 \_ Rect \_ F&, ID2D1Brush \* , D2D1 \_ Draw \_ Text \_ Options, DWRITE \_ Text \_ mediing \_ Method)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="233ae-109">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F&,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span>  | <span data-ttu-id="233ae-110">Dibuja el texto especificado utilizando la información de formato proporcionada por un objeto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="233ae-110">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span><br/>  |
| <span data-ttu-id="233ae-111">[**DrawText (WCHAR \* , IDWriteTextFormat \* , D2D1 \_ Rect \_ F \* , ID2D1Brush \* , D2D1 \_ Draw \_ Text \_ Options, DWRITE \_ Text \_ mediing \_ Method)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="233ae-111">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F\*,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span> | <span data-ttu-id="233ae-112">Dibuja el texto especificado utilizando la información de formato proporcionada por un objeto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="233ae-112">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="233ae-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="233ae-113">Remarks</span></span>

<span data-ttu-id="233ae-114">Para dibujar texto con Direct2D, use el método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) para el texto que tiene un formato único, o el método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) cuando necesite varios formatos, características OpenType avanzadas o pruebas de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="233ae-114">To draw text with Direct2D, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method for text that has a single format, or the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method when you need multiple formats, advanced OpenType features, or hit testing.</span></span> <span data-ttu-id="233ae-115">Estos métodos usan la API de DirectWrite para proporcionar una presentación de texto de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="233ae-115">These methods use the DirectWrite API to provide high-quality text display.</span></span>

<span data-ttu-id="233ae-116">Este método no devuelve un código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="233ae-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="233ae-117">Para determinar si una operación de dibujo (como **DrawText**) produjo un error, compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="233ae-117">To determine whether a drawing operation (such as **DrawText**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="233ae-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="233ae-118">Examples</span></span>

<span data-ttu-id="233ae-119">Para obtener un ejemplo, vea [Cómo dibujar texto](how-to--draw-text.md).</span><span class="sxs-lookup"><span data-stu-id="233ae-119">For an example, see [How to Draw Text](how-to--draw-text.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="233ae-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="233ae-120">Requirements</span></span>



| <span data-ttu-id="233ae-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="233ae-121">Requirement</span></span> | <span data-ttu-id="233ae-122">Value</span><span class="sxs-lookup"><span data-stu-id="233ae-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="233ae-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="233ae-123">Library</span></span><br/> | <dl> <span data-ttu-id="233ae-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="233ae-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="233ae-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="233ae-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="233ae-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="233ae-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="233ae-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="233ae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="233ae-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="233ae-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="233ae-129">**IDWriteTextFormat**</span><span class="sxs-lookup"><span data-stu-id="233ae-129">**IDWriteTextFormat**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[<span data-ttu-id="233ae-130">Cómo dibujar texto</span><span class="sxs-lookup"><span data-stu-id="233ae-130">How to Draw Text</span></span>](how-to--draw-text.md)
</dt> <dt>

[<span data-ttu-id="233ae-131">Información general sobre el diseño y el formato de texto</span><span class="sxs-lookup"><span data-stu-id="233ae-131">Text Formatting and Layout Overview</span></span>](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

