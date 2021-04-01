---
title: Mensaje de TB_INSERTBUTTON (commctrl. h)
description: Inserta un botón en una barra de herramientas.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- TB_INSERTBUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e08eed328a99d4a8927a7e09084bf122f2e4e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150124"
---
# <a name="tb_insertbutton-message"></a><span data-ttu-id="5a3fa-104">\_Mensaje INSERTBUTTON TB</span><span class="sxs-lookup"><span data-stu-id="5a3fa-104">TB\_INSERTBUTTON message</span></span>

<span data-ttu-id="5a3fa-105">Inserta un botón en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="5a3fa-105">Inserts a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a3fa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a3fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a3fa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a3fa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a3fa-108">Índice de base cero de un botón.</span><span class="sxs-lookup"><span data-stu-id="5a3fa-108">Zero-based index of a button.</span></span> <span data-ttu-id="5a3fa-109">El mensaje inserta el nuevo botón a la izquierda de este botón.</span><span class="sxs-lookup"><span data-stu-id="5a3fa-109">The message inserts the new button to the left of this button.</span></span>

</dd> <dt>

<span data-ttu-id="5a3fa-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a3fa-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a3fa-111">Puntero a una estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que contiene información sobre el botón que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="5a3fa-111">Pointer to a [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure containing information about the button to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a3fa-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a3fa-112">Return value</span></span>

<span data-ttu-id="5a3fa-113">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5a3fa-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a3fa-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a3fa-114">Requirements</span></span>



| <span data-ttu-id="5a3fa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a3fa-115">Requirement</span></span> | <span data-ttu-id="5a3fa-116">Value</span><span class="sxs-lookup"><span data-stu-id="5a3fa-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3fa-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a3fa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5a3fa-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5a3fa-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a3fa-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a3fa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5a3fa-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a3fa-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a3fa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a3fa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a3fa-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a3fa-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5a3fa-123">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="5a3fa-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5a3fa-124">**TB \_ INSERTBUTTONW** (Unicode) y **TB \_ INSERTBUTTONA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5a3fa-124">**TB\_INSERTBUTTONW** (Unicode) and **TB\_INSERTBUTTONA** (ANSI)</span></span><br/>           |



 

 





