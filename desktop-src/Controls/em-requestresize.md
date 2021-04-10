---
title: Mensaje EM_REQUESTRESIZE (RichEdit. h)
description: Fuerza a un control Rich Edit a enviar un \_ código de notificación en REQUESTRESIZE a su ventana primaria.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- EM_REQUESTRESIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274549"
---
# <a name="em_requestresize-message"></a><span data-ttu-id="914db-104">\_Mensaje REQUESTRESIZE em</span><span class="sxs-lookup"><span data-stu-id="914db-104">EM\_REQUESTRESIZE message</span></span>

<span data-ttu-id="914db-105">Fuerza a un control Rich Edit a enviar un código de notificación [**en \_ REQUESTRESIZE**](en-requestresize.md) a su ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="914db-105">Forces a rich edit control to send an [**EN\_REQUESTRESIZE**](en-requestresize.md) notification code to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="914db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="914db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="914db-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="914db-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="914db-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="914db-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="914db-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="914db-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="914db-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="914db-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="914db-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="914db-111">Return value</span></span>

<span data-ttu-id="914db-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="914db-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="914db-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="914db-113">Remarks</span></span>

<span data-ttu-id="914db-114">Este mensaje es útil durante el procesamiento de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) para el elemento primario de un control Rich Edit no completo.</span><span class="sxs-lookup"><span data-stu-id="914db-114">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="914db-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="914db-115">Requirements</span></span>



| <span data-ttu-id="914db-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="914db-116">Requirement</span></span> | <span data-ttu-id="914db-117">Value</span><span class="sxs-lookup"><span data-stu-id="914db-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="914db-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="914db-118">Minimum supported client</span></span><br/> | <span data-ttu-id="914db-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="914db-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="914db-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="914db-120">Minimum supported server</span></span><br/> | <span data-ttu-id="914db-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="914db-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="914db-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="914db-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="914db-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="914db-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="914db-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="914db-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="914db-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="914db-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="914db-126">**EN \_ REQUESTRESIZE**</span><span class="sxs-lookup"><span data-stu-id="914db-126">**EN\_REQUESTRESIZE**</span></span>](en-requestresize.md)
</dt> <dt>

<span data-ttu-id="914db-127">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="914db-127">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="914db-128">**tamaño de WM \_**</span><span class="sxs-lookup"><span data-stu-id="914db-128">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

