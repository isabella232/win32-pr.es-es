---
title: Mensaje de TB_HIDEBUTTON (commctrl. h)
description: Oculta o muestra el botón especificado en una barra de herramientas.
ms.assetid: 57941a40-279a-426e-baf9-115429c62839
keywords:
- TB_HIDEBUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_HIDEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e198a48ae65f13be699b76a20c9f423cdb0da197
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996212"
---
# <a name="tb_hidebutton-message"></a><span data-ttu-id="37dd8-104">\_Mensaje HIDEBUTTON TB</span><span class="sxs-lookup"><span data-stu-id="37dd8-104">TB\_HIDEBUTTON message</span></span>

<span data-ttu-id="37dd8-105">Oculta o muestra el botón especificado en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="37dd8-105">Hides or shows the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="37dd8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37dd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37dd8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37dd8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37dd8-108">Identificador de comando del botón que se va a ocultar o mostrar.</span><span class="sxs-lookup"><span data-stu-id="37dd8-108">Command identifier of the button to hide or show.</span></span>

</dd> <dt>

<span data-ttu-id="37dd8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37dd8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37dd8-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un **booleano** que indica si se va a ocultar o mostrar el botón especificado.</span><span class="sxs-lookup"><span data-stu-id="37dd8-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to hide or show the specified button.</span></span> <span data-ttu-id="37dd8-111">Si es **true**, el botón está oculto.</span><span class="sxs-lookup"><span data-stu-id="37dd8-111">If **TRUE**, the button is hidden.</span></span> <span data-ttu-id="37dd8-112">Si es **false**, se muestra el botón.</span><span class="sxs-lookup"><span data-stu-id="37dd8-112">If **FALSE**, the button is shown.</span></span>

<span data-ttu-id="37dd8-113">El valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="37dd8-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37dd8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37dd8-114">Return value</span></span>

<span data-ttu-id="37dd8-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="37dd8-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="37dd8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37dd8-116">Requirements</span></span>



| <span data-ttu-id="37dd8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="37dd8-117">Requirement</span></span> | <span data-ttu-id="37dd8-118">Value</span><span class="sxs-lookup"><span data-stu-id="37dd8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37dd8-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37dd8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="37dd8-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="37dd8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37dd8-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37dd8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="37dd8-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="37dd8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37dd8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37dd8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="37dd8-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="37dd8-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

