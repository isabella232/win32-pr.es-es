---
title: Mensaje de BM_CLICK (Winuser. h)
description: Simula que el usuario hace clic en un botón. Este mensaje hace que el botón reciba los mensajes de WM \_ LBUTTONDOWN y WM \_ LBUTTONUP, y la ventana primaria del botón para recibir un código de notificación en el que se ha \_ haga clic en BN.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- BM_CLICK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b86c4809ac1ded3a9b7c57d1b73b70ab1cebc3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079078"
---
# <a name="bm_click-message"></a><span data-ttu-id="3f5f9-105">Mensaje de clic de BM \_</span><span class="sxs-lookup"><span data-stu-id="3f5f9-105">BM\_CLICK message</span></span>

<span data-ttu-id="3f5f9-106">Simula que el usuario hace clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="3f5f9-106">Simulates the user clicking a button.</span></span> <span data-ttu-id="3f5f9-107">Este mensaje hace que el botón reciba los mensajes de [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) y [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) , y la ventana primaria del botón para recibir un código de notificación en el que se ha [ \_ haga clic en BN](bn-clicked.md) .</span><span class="sxs-lookup"><span data-stu-id="3f5f9-107">This message causes the button to receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) and [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages, and the button's parent window to receive a [BN\_CLICKED](bn-clicked.md) notification code.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f5f9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f5f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f5f9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f5f9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f5f9-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3f5f9-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3f5f9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f5f9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f5f9-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3f5f9-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f5f9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f5f9-113">Return value</span></span>

<span data-ttu-id="3f5f9-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3f5f9-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f5f9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f5f9-115">Remarks</span></span>

<span data-ttu-id="3f5f9-116">Si el botón está en un cuadro de diálogo y el cuadro de diálogo no está activo, puede producirse un error en el mensaje de **\_ clic de BM** .</span><span class="sxs-lookup"><span data-stu-id="3f5f9-116">If the button is in a dialog box and the dialog box is not active, the **BM\_CLICK** message might fail.</span></span> <span data-ttu-id="3f5f9-117">Para asegurarse de que se ha realizado correctamente en esta situación, llame a la función [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) para activar el cuadro de diálogo antes de enviar el mensaje de **\_ clic de BM** al botón.</span><span class="sxs-lookup"><span data-stu-id="3f5f9-117">To ensure success in this situation, call the [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) function to activate the dialog box before sending the **BM\_CLICK** message to the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f5f9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f5f9-118">Requirements</span></span>



| <span data-ttu-id="3f5f9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f5f9-119">Requirement</span></span> | <span data-ttu-id="3f5f9-120">Value</span><span class="sxs-lookup"><span data-stu-id="3f5f9-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f5f9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f5f9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3f5f9-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3f5f9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3f5f9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f5f9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3f5f9-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f5f9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3f5f9-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f5f9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f5f9-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f5f9-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

