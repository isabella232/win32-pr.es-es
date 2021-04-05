---
title: Mensaje de TB_INDETERMINATE (commctrl. h)
description: Establece o borra el estado indeterminado del botón especificado en una barra de herramientas.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- TB_INDETERMINATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_INDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f1de35f9621de4f51d371bb50dbda637d720cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079197"
---
# <a name="tb_indeterminate-message"></a><span data-ttu-id="2b5c8-104">TB de \_ mensaje indeterminado</span><span class="sxs-lookup"><span data-stu-id="2b5c8-104">TB\_INDETERMINATE message</span></span>

<span data-ttu-id="2b5c8-105">Establece o borra el estado indeterminado del botón especificado en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="2b5c8-105">Sets or clears the indeterminate state of the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b5c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b5c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b5c8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b5c8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b5c8-108">Identificador de comando del botón cuyo estado indeterminado se va a establecer o borrar.</span><span class="sxs-lookup"><span data-stu-id="2b5c8-108">Command identifier of the button whose indeterminate state is to be set or cleared.</span></span>

</dd> <dt>

<span data-ttu-id="2b5c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b5c8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b5c8-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un valor **booleano** que indica si se debe establecer o borrar el estado indeterminado.</span><span class="sxs-lookup"><span data-stu-id="2b5c8-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to set or clear the indeterminate state.</span></span> <span data-ttu-id="2b5c8-111">Si es **true**, se establece el estado indeterminado.</span><span class="sxs-lookup"><span data-stu-id="2b5c8-111">If **TRUE**, the indeterminate state is set.</span></span> <span data-ttu-id="2b5c8-112">Si es **false**, el estado es desactivado.</span><span class="sxs-lookup"><span data-stu-id="2b5c8-112">If **FALSE**, the state is cleared.</span></span>

<span data-ttu-id="2b5c8-113">El valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2b5c8-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b5c8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b5c8-114">Return value</span></span>

<span data-ttu-id="2b5c8-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2b5c8-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b5c8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b5c8-116">Requirements</span></span>



| <span data-ttu-id="2b5c8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b5c8-117">Requirement</span></span> | <span data-ttu-id="2b5c8-118">Value</span><span class="sxs-lookup"><span data-stu-id="2b5c8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b5c8-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b5c8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2b5c8-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2b5c8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b5c8-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b5c8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2b5c8-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b5c8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b5c8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b5c8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b5c8-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b5c8-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

