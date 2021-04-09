---
title: Mensaje de TB_CHECKBUTTON (commctrl. h)
description: Comprueba o desactiva un botón determinado en una barra de herramientas.
ms.assetid: e67734a9-851c-41ab-8ad7-15d434f58e5a
keywords:
- TB_CHECKBUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_CHECKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7734b37da44db38d9ca09b34ad9e666cc90eb5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079778"
---
# <a name="tb_checkbutton-message"></a><span data-ttu-id="13ed1-104">\_Mensaje CHECKBUTTON TB</span><span class="sxs-lookup"><span data-stu-id="13ed1-104">TB\_CHECKBUTTON message</span></span>

<span data-ttu-id="13ed1-105">Comprueba o desactiva un botón determinado en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="13ed1-105">Checks or unchecks a given button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="13ed1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13ed1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13ed1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13ed1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13ed1-108">Identificador de comando del botón que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="13ed1-108">Command identifier of the button to check.</span></span>

</dd> <dt>

<span data-ttu-id="13ed1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13ed1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13ed1-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un **booleano** que indica si se debe activar o desactivar el botón especificado.</span><span class="sxs-lookup"><span data-stu-id="13ed1-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to check or uncheck the specified button.</span></span> <span data-ttu-id="13ed1-111">Si es **true**, se agrega la comprobación.</span><span class="sxs-lookup"><span data-stu-id="13ed1-111">If **TRUE**, the check is added.</span></span> <span data-ttu-id="13ed1-112">Si es **false**, se quita la comprobación.</span><span class="sxs-lookup"><span data-stu-id="13ed1-112">If **FALSE**, the check is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13ed1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13ed1-113">Return value</span></span>

<span data-ttu-id="13ed1-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="13ed1-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="13ed1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13ed1-115">Remarks</span></span>

<span data-ttu-id="13ed1-116">Cuando se activa un botón, se muestra en estado presionado.</span><span class="sxs-lookup"><span data-stu-id="13ed1-116">When a button is checked, it is displayed in the pressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="13ed1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13ed1-117">Requirements</span></span>



| <span data-ttu-id="13ed1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="13ed1-118">Requirement</span></span> | <span data-ttu-id="13ed1-119">Value</span><span class="sxs-lookup"><span data-stu-id="13ed1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13ed1-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13ed1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="13ed1-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="13ed1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="13ed1-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13ed1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="13ed1-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="13ed1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="13ed1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13ed1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="13ed1-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="13ed1-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

