---
title: Mensaje de TB_ENABLEBUTTON (commctrl. h)
description: Habilita o deshabilita el botón especificado en una barra de herramientas.
ms.assetid: d73851ee-f909-4b70-9514-c45cd3a7e999
keywords:
- TB_ENABLEBUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_ENABLEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf2fe865d49f9c89e31b1701abfcbf7991ae72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658403"
---
# <a name="tb_enablebutton-message"></a><span data-ttu-id="ccdb9-104">\_Mensaje ENABLEBUTTON TB</span><span class="sxs-lookup"><span data-stu-id="ccdb9-104">TB\_ENABLEBUTTON message</span></span>

<span data-ttu-id="ccdb9-105">Habilita o deshabilita el botón especificado en una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="ccdb9-105">Enables or disables the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccdb9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ccdb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccdb9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccdb9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccdb9-108">Identificador de comando del botón que se va a habilitar o deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="ccdb9-108">Command identifier of the button to enable or disable.</span></span>

</dd> <dt>

<span data-ttu-id="ccdb9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccdb9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccdb9-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un **booleano** que indica si se debe habilitar o deshabilitar el botón especificado.</span><span class="sxs-lookup"><span data-stu-id="ccdb9-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to enable or disable the specified button.</span></span> <span data-ttu-id="ccdb9-111">Si es **true**, el botón está habilitado.</span><span class="sxs-lookup"><span data-stu-id="ccdb9-111">If **TRUE**, the button is enabled.</span></span> <span data-ttu-id="ccdb9-112">Si es **false**, el botón está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="ccdb9-112">If **FALSE**, the button is disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccdb9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ccdb9-113">Return value</span></span>

<span data-ttu-id="ccdb9-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ccdb9-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccdb9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ccdb9-115">Remarks</span></span>

<span data-ttu-id="ccdb9-116">Cuando se ha habilitado un botón, se puede presionar y activar.</span><span class="sxs-lookup"><span data-stu-id="ccdb9-116">When a button has been enabled, it can be pressed and checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccdb9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccdb9-117">Requirements</span></span>



| <span data-ttu-id="ccdb9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccdb9-118">Requirement</span></span> | <span data-ttu-id="ccdb9-119">Value</span><span class="sxs-lookup"><span data-stu-id="ccdb9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccdb9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccdb9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ccdb9-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ccdb9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ccdb9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccdb9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ccdb9-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ccdb9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ccdb9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ccdb9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccdb9-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccdb9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

