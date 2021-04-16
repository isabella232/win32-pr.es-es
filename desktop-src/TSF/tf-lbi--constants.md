---
title: Constantes de TF_LBI_ (Ctfutb. h)
description: Las constantes de TF \_ LBI \_ \ se usan con el método ITfLangBarItemSink de actualización para indicar qué elementos de la barra de idioma han cambiado.
ms.assetid: ed84012f-19ba-43b3-bbb5-7373ed174c33
topic_type:
- apiref
api_name:
- TF_LBI_ICON
- TF_LBI_TEXT
- TF_LBI_TOOLTIP
- TF_LBI_BITMAP
- TF_LBI_BALLOON
- TF_LBI_STATUS
- TF_LBI_BMPALL
- TF_LBI_BMPBTNALL
- TF_LBI_BTNALL
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72b69f1cb5a5b4a24e78a2bdc1ca0e7a9d79cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685949"
---
# <a name="tf_lbi_-constants"></a><span data-ttu-id="7b3d1-103">TF \_ LBI ( \_ \* constantes)</span><span class="sxs-lookup"><span data-stu-id="7b3d1-103">TF\_LBI\_\* Constants</span></span>

<span data-ttu-id="7b3d1-104">Las constantes \*\* \_ TF \_ \* LBI\* _ se usan con el método [ITfLangBarItemSink:: ALUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) para indicar qué elementos de la barra de idioma han cambiado.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-104">The \**TF\_LBI\_\** _ constants are used with the [ITfLangBarItemSink::OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) method to indicate which language bar items changed.</span></span>



| <span data-ttu-id="7b3d1-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="7b3d1-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="7b3d1-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b3d1-106">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <span data-ttu-id="7b3d1-107"><dt>_ \* TF \_ Icono de LBI \_ \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7b3d1-107"><dt>_\*TF\_LBI\_ICON\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                                                        | <span data-ttu-id="7b3d1-108">El icono del elemento ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-108">The icon of the item has changed.</span></span> <span data-ttu-id="7b3d1-109">La barra de idioma llama a [ITfLangBarItemButton:: GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) en respuesta a esta notificación.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-109">The language bar calls [ITfLangBarItemButton::GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) in response to this notification.</span></span><br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <span data-ttu-id="7b3d1-110"><dt>**TF \_ \_Texto LBI**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="7b3d1-110"><dt>**TF\_LBI\_TEXT**</dt> <dt>0x00000002</dt></span></span> </dl>                                                        | <span data-ttu-id="7b3d1-111">El texto de un botón o elemento de botón de mapa de bits ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-111">The text of a button or bitmap button item has changed.</span></span> <span data-ttu-id="7b3d1-112">La barra de idioma llama a [ITfLangBarItemButton:: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) o [ITfLangBarItemBitmapButton:: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), lo que sea adecuado, en respuesta a esta notificación.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-112">The language bar calls [ITfLangBarItemButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) or [ITfLangBarItemBitmapButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), whichever is appropriate, in response to this notification.</span></span><br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <span data-ttu-id="7b3d1-113"><dt>**TF \_ \_Información sobre herramientas de LBI**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="7b3d1-113"><dt>**TF\_LBI\_TOOLTIP**</dt> <dt>0x00000004</dt></span></span> </dl>                                               | <span data-ttu-id="7b3d1-114">Texto de información sobre herramientas del elemento cambiado.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-114">The tooltip text of the item changed.</span></span> <span data-ttu-id="7b3d1-115">La barra de idioma llama a [ITfLangBarItem:: GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) en respuesta a esta notificación.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-115">The language bar calls [ITfLangBarItem::GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) in response to this notification.</span></span><br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <span data-ttu-id="7b3d1-116"><dt>**TF \_ \_Mapa de bits de LBI**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="7b3d1-116"><dt>**TF\_LBI\_BITMAP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                  | <span data-ttu-id="7b3d1-117">El mapa de bits de un mapa de bits o un elemento de botón de mapa de bits cambiado.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-117">The bitmap of a bitmap or bitmap button item changed.</span></span> <span data-ttu-id="7b3d1-118">La barra de idioma llama a [ITfLangBarItemBitmap::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) o [ITfLangBarItemBitmapButton::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), según corresponda, en respuesta a esta notificación.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-118">The language bar calls [ITfLangBarItemBitmap::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) or [ITfLangBarItemBitmapButton::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), whichever is appropriate, in response to this notification.</span></span><br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <span data-ttu-id="7b3d1-119"><dt>**TF \_ El \_ globo LBI**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="7b3d1-119"><dt>**TF\_LBI\_BALLOON**</dt> <dt>0x00000010</dt></span></span> </dl>                                               | <span data-ttu-id="7b3d1-120">La información de un elemento de globo ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-120">The information for a balloon item changed.</span></span> <span data-ttu-id="7b3d1-121">La barra de idioma llama a [ITfLangBarItemBalloon:: GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) en respuesta a esta notificación.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-121">The language bar calls [ITfLangBarItemBalloon::GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) in response to this notification.</span></span><br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <span data-ttu-id="7b3d1-122"><dt>**TF \_ 0x00010000 de \_ Estado de LBI**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7b3d1-122"><dt>**TF\_LBI\_STATUS**</dt> <dt>0x00010000</dt></span></span> </dl>                                                  | <span data-ttu-id="7b3d1-123">El estado del elemento ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-123">The item status changed.</span></span> <span data-ttu-id="7b3d1-124">La barra de idioma llama a [ITfLangBarItem:: getStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) en respuesta a esta notificación.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-124">The language bar calls [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) in response to this notification.</span></span><br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <span data-ttu-id="7b3d1-125"><dt>**TF \_ LBI \_ BMPALL**</dt> <dt>TF \_ LBI \_ mapa de bits \| TF \_ LBI \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="7b3d1-125"><dt>**TF\_LBI\_BMPALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>                          | <span data-ttu-id="7b3d1-126">Combina la \_ \_ información sobre herramientas TF LBI Bitmap y TF \_ LBI \_ .</span><span class="sxs-lookup"><span data-stu-id="7b3d1-126">Combines TF\_LBI\_BITMAP and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <span data-ttu-id="7b3d1-127"><dt>**TF \_ LBI \_ BMPBTNALL**</dt> <dt>TF \_ LBI \_ Bitmap \| TF \_ LBI \_ texto \| TF \_ LBI \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="7b3d1-127"><dt>**TF\_LBI\_BMPBTNALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl> | <span data-ttu-id="7b3d1-128">Combina los \_ \_ mapas de bits de TF LBI, TF \_ LBI \_ Text y TF \_ LBI \_ TOOLTIP.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-128">Combines TF\_LBI\_BITMAP, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <span data-ttu-id="7b3d1-129"><dt>**TF \_ LBI \_ BTNALL**</dt> <dt>TF \_ LBI \_ Icon \| TF \_ LBI \_ Text \| TF \_ LBI \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="7b3d1-129"><dt>**TF\_LBI\_BTNALL**</dt> <dt>TF\_LBI\_ICON\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>            | <span data-ttu-id="7b3d1-130">Combina el \_ \_ icono de TF LBI, TF \_ LBI \_ Text y TF \_ LBI \_ TOOLTIP.</span><span class="sxs-lookup"><span data-stu-id="7b3d1-130">Combines TF\_LBI\_ICON, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="7b3d1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b3d1-131">Requirements</span></span>



| <span data-ttu-id="7b3d1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b3d1-132">Requirement</span></span> | <span data-ttu-id="7b3d1-133">Value</span><span class="sxs-lookup"><span data-stu-id="7b3d1-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b3d1-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b3d1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7b3d1-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7b3d1-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7b3d1-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b3d1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7b3d1-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7b3d1-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7b3d1-138">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7b3d1-138">Redistributable</span></span><br/>          | <span data-ttu-id="7b3d1-139">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7b3d1-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="7b3d1-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b3d1-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b3d1-141"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b3d1-141"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b3d1-142">IDL</span><span class="sxs-lookup"><span data-stu-id="7b3d1-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7b3d1-143"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7b3d1-143"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b3d1-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b3d1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b3d1-145">ITfLangBarItemSink:: actualización</span><span class="sxs-lookup"><span data-stu-id="7b3d1-145">ITfLangBarItemSink::OnUpdate</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 





