---
title: Mensaje de LVM_GETTEXTCOLOR (commctrl. h)
description: Recupera el color del texto de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetTextColor de ListView.
ms.assetid: 51685e61-dd0a-4c21-8c66-31cf72c2b3e4
keywords:
- LVM_GETTEXTCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7686e8f06f49dbfc14899f47ba52017daaf23c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658336"
---
# <a name="lvm_gettextcolor-message"></a><span data-ttu-id="20b9a-105">\_Mensaje GETTEXTCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="20b9a-105">LVM\_GETTEXTCOLOR message</span></span>

<span data-ttu-id="20b9a-106">Recupera el color del texto de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="20b9a-106">Retrieves the text color of a list-view control.</span></span> <span data-ttu-id="20b9a-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetTextColor de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) .</span><span class="sxs-lookup"><span data-stu-id="20b9a-107">You can send this message explicitly or by using the [**ListView\_GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="20b9a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20b9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20b9a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="20b9a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="20b9a-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="20b9a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="20b9a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="20b9a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="20b9a-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="20b9a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20b9a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20b9a-113">Return value</span></span>

<span data-ttu-id="20b9a-114">Devuelve el color del texto.</span><span class="sxs-lookup"><span data-stu-id="20b9a-114">Returns the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="20b9a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20b9a-115">Requirements</span></span>



| <span data-ttu-id="20b9a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="20b9a-116">Requirement</span></span> | <span data-ttu-id="20b9a-117">Value</span><span class="sxs-lookup"><span data-stu-id="20b9a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20b9a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20b9a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="20b9a-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="20b9a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="20b9a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20b9a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="20b9a-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="20b9a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="20b9a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20b9a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="20b9a-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="20b9a-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





