---
title: Mensaje EM_HIDESELECTION (RichEdit. h)
description: El \_ mensaje HIDESELECTION de EM oculta o muestra la selección en un control Rich Edit.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- EM_HIDESELECTION controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a5690e52c2a25f5a359de205ac1584e1ef45ed4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996004"
---
# <a name="em_hideselection-message"></a><span data-ttu-id="ff77d-104">\_Mensaje de HIDESELECTION em</span><span class="sxs-lookup"><span data-stu-id="ff77d-104">EM\_HIDESELECTION message</span></span>

<span data-ttu-id="ff77d-105">El **mensaje \_ HIDESELECTION de EM** oculta o muestra la selección en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ff77d-105">The **EM\_HIDESELECTION** message hides or shows the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff77d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff77d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff77d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff77d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff77d-108">Valor que especifica si se va a ocultar o Mostrar la selección.</span><span class="sxs-lookup"><span data-stu-id="ff77d-108">Value specifying whether to hide or show the selection.</span></span> <span data-ttu-id="ff77d-109">Si este parámetro es cero, se muestra la selección.</span><span class="sxs-lookup"><span data-stu-id="ff77d-109">If this parameter is zero, the selection is shown.</span></span> <span data-ttu-id="ff77d-110">De lo contrario, la selección está oculta.</span><span class="sxs-lookup"><span data-stu-id="ff77d-110">Otherwise, the selection is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="ff77d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff77d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff77d-112">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ff77d-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff77d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff77d-113">Return value</span></span>

<span data-ttu-id="ff77d-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ff77d-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff77d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff77d-115">Requirements</span></span>



| <span data-ttu-id="ff77d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff77d-116">Requirement</span></span> | <span data-ttu-id="ff77d-117">Value</span><span class="sxs-lookup"><span data-stu-id="ff77d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff77d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff77d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ff77d-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ff77d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff77d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff77d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ff77d-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff77d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff77d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff77d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff77d-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff77d-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 





