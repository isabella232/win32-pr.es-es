---
title: Mensaje de ACM_ISPLAYING (commctrl. h)
description: Comprueba si se está reproduciendo un Audio-Video clip intercalado (AVI). Puede enviar este mensaje explícitamente o utilizar la macro Animate \_ IsPlaying.
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- ACM_ISPLAYING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- ACM_ISPLAYING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f663872ce02b9520e3e033cb5bc5a3da12bb3c3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079081"
---
# <a name="acm_isplaying-message"></a><span data-ttu-id="df758-105">\_Mensaje ISPLAYING de ACM</span><span class="sxs-lookup"><span data-stu-id="df758-105">ACM\_ISPLAYING message</span></span>

<span data-ttu-id="df758-106">Comprueba si se está reproduciendo un Audio-Video clip intercalado (AVI).</span><span class="sxs-lookup"><span data-stu-id="df758-106">Checks whether an Audio-Video Interleaved (AVI) clip is playing.</span></span> <span data-ttu-id="df758-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Animate \_ IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) .</span><span class="sxs-lookup"><span data-stu-id="df758-107">You can send this message explicitly or use the [**Animate\_IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="df758-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df758-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df758-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df758-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df758-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="df758-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="df758-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df758-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df758-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="df758-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df758-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df758-113">Return value</span></span>

<span data-ttu-id="df758-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="df758-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="df758-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df758-115">Requirements</span></span>



| <span data-ttu-id="df758-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="df758-116">Requirement</span></span> | <span data-ttu-id="df758-117">Value</span><span class="sxs-lookup"><span data-stu-id="df758-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df758-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df758-118">Minimum supported client</span></span><br/> | <span data-ttu-id="df758-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="df758-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df758-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df758-120">Minimum supported server</span></span><br/> | <span data-ttu-id="df758-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="df758-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df758-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df758-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="df758-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="df758-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





