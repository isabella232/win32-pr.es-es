---
title: Mensaje de EM_GETCUEBANNER (commctrl. h)
description: Obtiene el texto que se muestra como indicación textual, o sugerencia, en un control de edición.
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- EM_GETCUEBANNER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d28d4aeea5a206c74f2e6b41cee27b5073448ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997071"
---
# <a name="em_getcuebanner-message"></a><span data-ttu-id="57917-104">\_Mensaje GETCUEBANNER em</span><span class="sxs-lookup"><span data-stu-id="57917-104">EM\_GETCUEBANNER message</span></span>

<span data-ttu-id="57917-105">Obtiene el texto que se muestra como indicación textual, o sugerencia, en un control de edición.</span><span class="sxs-lookup"><span data-stu-id="57917-105">Gets the text that is displayed as the textual cue, or tip, in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="57917-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57917-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57917-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57917-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57917-108">Un puntero a un búfer Unicode que recibe el conjunto de texto como indicación textual.</span><span class="sxs-lookup"><span data-stu-id="57917-108">A pointer to a Unicode buffer that receives the text set as the textual cue.</span></span> <span data-ttu-id="57917-109">El autor de la llamada es responsable de la asignación del búfer.</span><span class="sxs-lookup"><span data-stu-id="57917-109">The caller is responsible for allocating the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="57917-110">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57917-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57917-111">Tamaño del búfer al que apunta *wParam* en **WCHARs**, incluido el **valor null** final.</span><span class="sxs-lookup"><span data-stu-id="57917-111">The size of the buffer pointed to by *wParam* in **WCHARs**, including the terminating **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57917-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57917-112">Return value</span></span>

<span data-ttu-id="57917-113">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="57917-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="57917-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57917-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="57917-115">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="57917-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="57917-116">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="57917-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="57917-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57917-117">Requirements</span></span>



| <span data-ttu-id="57917-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="57917-118">Requirement</span></span> | <span data-ttu-id="57917-119">Value</span><span class="sxs-lookup"><span data-stu-id="57917-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57917-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57917-120">Minimum supported client</span></span><br/> | <span data-ttu-id="57917-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="57917-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57917-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57917-122">Minimum supported server</span></span><br/> | <span data-ttu-id="57917-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="57917-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57917-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57917-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="57917-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="57917-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57917-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="57917-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57917-127">**Editar \_ GetCueBannerText**</span><span class="sxs-lookup"><span data-stu-id="57917-127">**Edit\_GetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





