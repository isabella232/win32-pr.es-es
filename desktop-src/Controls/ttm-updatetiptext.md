---
title: Mensaje de TTM_UPDATETIPTEXT (commctrl. h)
description: Establece el texto de la información sobre herramientas de una herramienta.
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- TTM_UPDATETIPTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_UPDATETIPTEXT
- TTM_UPDATETIPTEXTA
- TTM_UPDATETIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c94b14ec83c190ce019ecba1413d2fa05f0103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150537"
---
# <a name="ttm_updatetiptext-message"></a><span data-ttu-id="e363b-104">TTM \_ UPDATETIPTEXT</span><span class="sxs-lookup"><span data-stu-id="e363b-104">TTM\_UPDATETIPTEXT message</span></span>

<span data-ttu-id="e363b-105">Establece el texto de la información sobre herramientas de una herramienta.</span><span class="sxs-lookup"><span data-stu-id="e363b-105">Sets the tooltip text for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="e363b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e363b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e363b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e363b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e363b-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e363b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e363b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e363b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e363b-110">Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="e363b-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="e363b-111">Los miembros **HINST** y **lpszText** deben especificar el identificador de instancia y la dirección del texto.</span><span class="sxs-lookup"><span data-stu-id="e363b-111">The **hinst** and **lpszText** members must specify the instance handle and the address of the text.</span></span> <span data-ttu-id="e363b-112">Los miembros **hWnd** y **uId** identifican la herramienta que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="e363b-112">The **hwnd** and **uId** members identify the tool to update.</span></span> <span data-ttu-id="e363b-113">El miembro **cbSize** de esta estructura se debe rellenar antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="e363b-113">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e363b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e363b-114">Return value</span></span>

<span data-ttu-id="e363b-115">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e363b-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e363b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e363b-116">Requirements</span></span>



| <span data-ttu-id="e363b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e363b-117">Requirement</span></span> | <span data-ttu-id="e363b-118">Value</span><span class="sxs-lookup"><span data-stu-id="e363b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e363b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e363b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e363b-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e363b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e363b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e363b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e363b-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e363b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e363b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e363b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e363b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e363b-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e363b-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="e363b-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e363b-126">**TTM \_ UPDATETIPTEXTW** (Unicode) y **TTM \_ UPDATETIPTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e363b-126">**TTM\_UPDATETIPTEXTW** (Unicode) and **TTM\_UPDATETIPTEXTA** (ANSI)</span></span><br/>       |



 

 





