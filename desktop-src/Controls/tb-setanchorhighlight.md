---
title: Mensaje de TB_SETANCHORHIGHLIGHT (commctrl. h)
description: Establece la configuración de resaltado de delimitador de una barra de herramientas.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- TB_SETANCHORHIGHLIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809f71e446f7768d637258152db1dd2d56346dfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656465"
---
# <a name="tb_setanchorhighlight-message"></a><span data-ttu-id="91f65-104">\_Mensaje SETANCHORHIGHLIGHT TB</span><span class="sxs-lookup"><span data-stu-id="91f65-104">TB\_SETANCHORHIGHLIGHT message</span></span>

<span data-ttu-id="91f65-105">Establece la configuración de resaltado de delimitador de una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="91f65-105">Sets the anchor highlight setting for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="91f65-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91f65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91f65-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91f65-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91f65-108">Valor **booleano** que especifica si está habilitado o deshabilitado el resaltado de delimitadores.</span><span class="sxs-lookup"><span data-stu-id="91f65-108">**BOOL** value that specifies if anchor highlighting is enabled or disabled.</span></span> <span data-ttu-id="91f65-109">Si este valor es distinto de cero, se habilitará el resaltado de delimitadores.</span><span class="sxs-lookup"><span data-stu-id="91f65-109">If this value is nonzero, anchor highlighting will be enabled.</span></span> <span data-ttu-id="91f65-110">Si este valor es cero, se deshabilitará el resaltado de delimitadores.</span><span class="sxs-lookup"><span data-stu-id="91f65-110">If this value is zero, anchor highlighting will be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="91f65-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91f65-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="91f65-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="91f65-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91f65-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91f65-113">Return value</span></span>

<span data-ttu-id="91f65-114">Devuelve el valor anterior de resaltado de delimitador.</span><span class="sxs-lookup"><span data-stu-id="91f65-114">Returns the previous anchor highlight setting.</span></span> <span data-ttu-id="91f65-115">Si este valor es distinto de cero, se ha habilitado el resaltado de delimitadores.</span><span class="sxs-lookup"><span data-stu-id="91f65-115">If this value is nonzero, anchor highlighting was enabled.</span></span> <span data-ttu-id="91f65-116">Si este valor es cero, se deshabilitó el resaltado de delimitadores.</span><span class="sxs-lookup"><span data-stu-id="91f65-116">If this value is zero, anchor highlighting was disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="91f65-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91f65-117">Remarks</span></span>

<span data-ttu-id="91f65-118">El resaltado de delimitadores en una barra de herramientas significa que el último elemento resaltado permanecerá resaltado hasta que se resalte otro elemento.</span><span class="sxs-lookup"><span data-stu-id="91f65-118">Anchor highlighting in a toolbar means that the last highlighted item will remain highlighted until another item is highlighted.</span></span> <span data-ttu-id="91f65-119">Esto sucede incluso si el cursor deja el control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="91f65-119">This occurs even if the cursor leaves the toolbar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="91f65-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91f65-120">Requirements</span></span>



| <span data-ttu-id="91f65-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="91f65-121">Requirement</span></span> | <span data-ttu-id="91f65-122">Value</span><span class="sxs-lookup"><span data-stu-id="91f65-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91f65-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91f65-123">Minimum supported client</span></span><br/> | <span data-ttu-id="91f65-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="91f65-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91f65-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91f65-125">Minimum supported server</span></span><br/> | <span data-ttu-id="91f65-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="91f65-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91f65-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91f65-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="91f65-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91f65-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





