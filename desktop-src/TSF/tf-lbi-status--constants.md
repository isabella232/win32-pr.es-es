---
title: Constantes de TF_LBI_STATUS_ (Ctfutb. h)
description: Las constantes de TF \_ LBI \_ status \_ indican el estado de un elemento de la barra de idioma. Estos valores se usan con el método GetStatus de ITfLangBarItem.
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803343"
---
# <a name="tf_lbi_status_-constants"></a><span data-ttu-id="41516-104">TF \_ LBI \_ ( \_ constantes de estado) \*</span><span class="sxs-lookup"><span data-stu-id="41516-104">TF\_LBI\_STATUS\_\* Constants</span></span>

<span data-ttu-id="41516-105">Las constantes \*\* \_ TF \_ LBI \_ \* status\* _ indican el estado de un elemento de la barra de idioma.</span><span class="sxs-lookup"><span data-stu-id="41516-105">The \**TF\_LBI\_STATUS\_\** _ constants indicate the status of a language bar item.</span></span> <span data-ttu-id="41516-106">Estos valores se usan con el método [ITfLangBarItem:: getStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) .</span><span class="sxs-lookup"><span data-stu-id="41516-106">These values are used with the [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) method.</span></span>



| <span data-ttu-id="41516-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="41516-107">Constant/value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="41516-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="41516-108">Description</span></span>                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <span data-ttu-id="41516-109"><dt>_ \* TF \_ Estado de LBI \_ \_ oculto \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="41516-109"><dt>_\*TF\_LBI\_STATUS\_HIDDEN\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="41516-110">El elemento está oculto.</span><span class="sxs-lookup"><span data-stu-id="41516-110">The item is hidden.</span></span> <span data-ttu-id="41516-111">Este estilo se omite si el elemento no incluye el \_ estilo HIDDENSTATUSCONTROL de TF LBI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="41516-111">This style is ignored if the item does not include the TF\_LBI\_STYLE\_HIDDENSTATUSCONTROL style.</span></span><br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <span data-ttu-id="41516-112"><dt>**TF \_ Estado de LBI \_ \_ deshabilitado**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="41516-112"><dt>**TF\_LBI\_STATUS\_DISABLED**</dt> <dt>0x00000002</dt></span></span> </dl>           | <span data-ttu-id="41516-113">El elemento está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="41516-113">The item is disabled.</span></span><br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <span data-ttu-id="41516-114"><dt>**TF \_ Estado de LBI \_ \_ BTN \_**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="41516-114"><dt>**TF\_LBI\_STATUS\_BTN\_TOGGLED**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="41516-115">El elemento está en el estado de alternado u presionado.</span><span class="sxs-lookup"><span data-stu-id="41516-115">The item is in the toggled or pressed state.</span></span> <span data-ttu-id="41516-116">Este estilo se omite si el elemento no incluye el estilo de alternancia de tipo de comando TF \_ LBI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="41516-116">This style is ignored if the item does not include the TF\_LBI\_STYLE\_BTN\_TOGGLE style.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="41516-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41516-117">Requirements</span></span>



| <span data-ttu-id="41516-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="41516-118">Requirement</span></span> | <span data-ttu-id="41516-119">Value</span><span class="sxs-lookup"><span data-stu-id="41516-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41516-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41516-120">Minimum supported client</span></span><br/> | <span data-ttu-id="41516-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="41516-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="41516-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41516-122">Minimum supported server</span></span><br/> | <span data-ttu-id="41516-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="41516-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41516-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="41516-124">Redistributable</span></span><br/>          | <span data-ttu-id="41516-125">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="41516-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="41516-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41516-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="41516-127"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="41516-127"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="41516-128">IDL</span><span class="sxs-lookup"><span data-stu-id="41516-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41516-129"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41516-129"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41516-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="41516-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41516-131">ITfLangBarItem:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="41516-131">ITfLangBarItem::GetStatus</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





