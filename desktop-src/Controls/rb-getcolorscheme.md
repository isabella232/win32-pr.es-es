---
title: Mensaje de RB_GETCOLORSCHEME (commctrl. h)
description: Recupera la información de la combinación de colores del control rebar.
ms.assetid: 01f81c4b-bbc9-43ae-a1f5-1e289c6fa278
keywords:
- RB_GETCOLORSCHEME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d154fd14b93127aa22148f2882f70018225cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534665"
---
# <a name="rb_getcolorscheme-message"></a><span data-ttu-id="b5750-104">Mensaje de GETCOLORSCHEME de RB \_</span><span class="sxs-lookup"><span data-stu-id="b5750-104">RB\_GETCOLORSCHEME message</span></span>

<span data-ttu-id="b5750-105">Recupera la información de la combinación de colores del control rebar.</span><span class="sxs-lookup"><span data-stu-id="b5750-105">Retrieves the color scheme information from the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5750-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5750-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5750-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5750-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b5750-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b5750-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b5750-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5750-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5750-110">Puntero a una estructura [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que recibirá la información de la combinación de colores.</span><span class="sxs-lookup"><span data-stu-id="b5750-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that will receive the color scheme information.</span></span> <span data-ttu-id="b5750-111">Debe establecer el miembro **dwSize** de esta estructura en **sizeof**(COLORSCHEME) antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b5750-111">You must set the **dwSize** member of this structure to **sizeof**(COLORSCHEME) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5750-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5750-112">Return value</span></span>

<span data-ttu-id="b5750-113">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="b5750-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5750-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5750-114">Requirements</span></span>



| <span data-ttu-id="b5750-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5750-115">Requirement</span></span> | <span data-ttu-id="b5750-116">Value</span><span class="sxs-lookup"><span data-stu-id="b5750-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5750-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5750-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b5750-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b5750-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5750-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5750-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b5750-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5750-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5750-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5750-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5750-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5750-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5750-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5750-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5750-124">**\_SETCOLORSCHEME RB**</span><span class="sxs-lookup"><span data-stu-id="b5750-124">**RB\_SETCOLORSCHEME**</span></span>](rb-setcolorscheme.md)
</dt> </dl>

 

 





