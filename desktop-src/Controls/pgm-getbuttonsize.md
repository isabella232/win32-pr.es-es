---
title: Mensaje de PGM_GETBUTTONSIZE (commctrl. h)
description: Recupera el tamaño actual del botón para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro GetButtonSize de buscapersonas \_ .
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- PGM_GETBUTTONSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5cb36d203aaeae748db9adb1b13cacf2e40f5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079561"
---
# <a name="pgm_getbuttonsize-message"></a><span data-ttu-id="c9ebc-105">\_Mensaje GETBUTTONSIZE PGM</span><span class="sxs-lookup"><span data-stu-id="c9ebc-105">PGM\_GETBUTTONSIZE message</span></span>

<span data-ttu-id="c9ebc-106">Recupera el tamaño actual del botón para el control de paginación.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-106">Retrieves the current button size for the pager control.</span></span> <span data-ttu-id="c9ebc-107">Puede enviar este mensaje explícitamente o utilizar la macro [**\_ GetButtonSize de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) .</span><span class="sxs-lookup"><span data-stu-id="c9ebc-107">You can send this message explicitly or use the [**Pager\_GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9ebc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9ebc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9ebc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9ebc-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c9ebc-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c9ebc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9ebc-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c9ebc-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9ebc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9ebc-113">Return value</span></span>

<span data-ttu-id="c9ebc-114">Devuelve un valor INT que contiene el tamaño del botón actual, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c9ebc-114">Returns an INT value that contains the current button size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9ebc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9ebc-115">Requirements</span></span>



| <span data-ttu-id="c9ebc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9ebc-116">Requirement</span></span> | <span data-ttu-id="c9ebc-117">Value</span><span class="sxs-lookup"><span data-stu-id="c9ebc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ebc-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9ebc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c9ebc-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c9ebc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9ebc-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9ebc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c9ebc-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9ebc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9ebc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9ebc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9ebc-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9ebc-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9ebc-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9ebc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9ebc-125">**\_SETBUTTONSIZE PGM**</span><span class="sxs-lookup"><span data-stu-id="c9ebc-125">**PGM\_SETBUTTONSIZE**</span></span>](pgm-setbuttonsize.md)
</dt> </dl>

 

 





