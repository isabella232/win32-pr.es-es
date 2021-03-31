---
title: Mensaje de TB_GETCOLORSCHEME (commctrl. h)
description: Recupera la información de la combinación de colores del control de barra de herramientas.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- TB_GETCOLORSCHEME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61344439ae8bc2b3a9ecd47472174577d652aa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490997"
---
# <a name="tb_getcolorscheme-message"></a><span data-ttu-id="4fba3-104">\_Mensaje GETCOLORSCHEME TB</span><span class="sxs-lookup"><span data-stu-id="4fba3-104">TB\_GETCOLORSCHEME message</span></span>

<span data-ttu-id="4fba3-105">Recupera la información de la combinación de colores del control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="4fba3-105">Retrieves the color scheme information from the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4fba3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fba3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fba3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4fba3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4fba3-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4fba3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4fba3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4fba3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fba3-110">Puntero a una estructura [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que recibirá la información de la combinación de colores.</span><span class="sxs-lookup"><span data-stu-id="4fba3-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that will receive the color scheme information.</span></span> <span data-ttu-id="4fba3-111">Debe establecer el miembro **cbSize** de esta estructura en **sizeof**(COLORSCHEME) antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="4fba3-111">You must set the **cbSize** member of this structure to **sizeof**(COLORSCHEME) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fba3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fba3-112">Return value</span></span>

<span data-ttu-id="4fba3-113">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="4fba3-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fba3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fba3-114">Requirements</span></span>



| <span data-ttu-id="4fba3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fba3-115">Requirement</span></span> | <span data-ttu-id="4fba3-116">Value</span><span class="sxs-lookup"><span data-stu-id="4fba3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4fba3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fba3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4fba3-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4fba3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4fba3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fba3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4fba3-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4fba3-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4fba3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fba3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fba3-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fba3-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fba3-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fba3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fba3-124">**TB \_ SETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="4fba3-124">**TB\_SETCOLORSCHEME**</span></span>](tb-setcolorscheme.md)
</dt> </dl>

 

 





