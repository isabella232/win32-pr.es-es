---
title: Mensaje de TB_PRESSBUTTON (commctrl. h)
description: Presiona o suelta el botón especificado en una barra de herramientas.
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- TB_PRESSBUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_PRESSBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0e86092951b242cee7388fc0d5d1bbdbca835e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150740"
---
# <a name="tb_pressbutton-message"></a><span data-ttu-id="fce0f-104">\_Mensaje PRESSBUTTON TB</span><span class="sxs-lookup"><span data-stu-id="fce0f-104">TB\_PRESSBUTTON message</span></span>

<span data-ttu-id="fce0f-105">Presiona o suelta el botón especificado en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="fce0f-105">Presses or releases the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="fce0f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fce0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fce0f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fce0f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fce0f-108">Identificador de comando del botón que se va a presionar o liberar.</span><span class="sxs-lookup"><span data-stu-id="fce0f-108">Command identifier of the button to press or release.</span></span>

</dd> <dt>

<span data-ttu-id="fce0f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fce0f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fce0f-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un **booleano** que indica si se debe presionar o liberar el botón especificado.</span><span class="sxs-lookup"><span data-stu-id="fce0f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to press or release the specified button.</span></span> <span data-ttu-id="fce0f-111">Si es **true**, el botón está presionado.</span><span class="sxs-lookup"><span data-stu-id="fce0f-111">If **TRUE**, the button is pressed.</span></span> <span data-ttu-id="fce0f-112">Si es **false**, se libera el botón.</span><span class="sxs-lookup"><span data-stu-id="fce0f-112">If **FALSE**, the button is released.</span></span>

<span data-ttu-id="fce0f-113">El valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fce0f-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fce0f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fce0f-114">Return value</span></span>

<span data-ttu-id="fce0f-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fce0f-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce0f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fce0f-116">Requirements</span></span>



| <span data-ttu-id="fce0f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fce0f-117">Requirement</span></span> | <span data-ttu-id="fce0f-118">Value</span><span class="sxs-lookup"><span data-stu-id="fce0f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fce0f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fce0f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fce0f-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fce0f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fce0f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fce0f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fce0f-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fce0f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fce0f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fce0f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fce0f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fce0f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

