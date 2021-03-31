---
title: Mensaje de BM_SETSTYLE (Winuser. h)
description: Establece el estilo de un botón. Puede enviar este mensaje explícitamente o usar el botón \_ setStyle macro.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- BM_SETSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996115"
---
# <a name="bm_setstyle-message"></a><span data-ttu-id="697aa-105">\_Mensaje SETSTYLE de BM</span><span class="sxs-lookup"><span data-stu-id="697aa-105">BM\_SETSTYLE message</span></span>

<span data-ttu-id="697aa-106">Establece el estilo de un botón.</span><span class="sxs-lookup"><span data-stu-id="697aa-106">Sets the style of a button.</span></span> <span data-ttu-id="697aa-107">Puede enviar este mensaje explícitamente o usar el [**botón \_ setStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) macro.</span><span class="sxs-lookup"><span data-stu-id="697aa-107">You can send this message explicitly or use the [**Button\_SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="697aa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="697aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="697aa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="697aa-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="697aa-110">Estilo de botón.</span><span class="sxs-lookup"><span data-stu-id="697aa-110">The button style.</span></span> <span data-ttu-id="697aa-111">Este parámetro puede ser una combinación de estilos de botón.</span><span class="sxs-lookup"><span data-stu-id="697aa-111">This parameter can be a combination of button styles.</span></span> <span data-ttu-id="697aa-112">Para obtener una tabla de estilos de botón, consulte [estilos de botón](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="697aa-112">For a table of button styles, see [Button Styles](button-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="697aa-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="697aa-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="697aa-114">El [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* es un **booleano** que especifica si se debe volver a dibujar el botón.</span><span class="sxs-lookup"><span data-stu-id="697aa-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* is a **BOOL** that specifies whether the button is to be redrawn.</span></span> <span data-ttu-id="697aa-115">Un valor de **true** vuelve a dibujar el botón; un valor **false** no vuelve a dibujar el botón.</span><span class="sxs-lookup"><span data-stu-id="697aa-115">A value of **TRUE** redraws the button; a value of **FALSE** does not redraw the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="697aa-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="697aa-116">Return value</span></span>

<span data-ttu-id="697aa-117">Este mensaje siempre devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="697aa-117">This message always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="697aa-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="697aa-118">Requirements</span></span>



| <span data-ttu-id="697aa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="697aa-119">Requirement</span></span> | <span data-ttu-id="697aa-120">Value</span><span class="sxs-lookup"><span data-stu-id="697aa-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="697aa-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="697aa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="697aa-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="697aa-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="697aa-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="697aa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="697aa-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="697aa-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="697aa-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="697aa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="697aa-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="697aa-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

