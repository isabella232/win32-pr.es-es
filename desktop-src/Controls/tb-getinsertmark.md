---
title: Mensaje de TB_GETINSERTMARK (commctrl. h)
description: Recupera la marca de inserción actual de la barra de herramientas.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- TB_GETINSERTMARK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45a4cafbd49c709e9ca5b8e9afeda51323de491
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078996"
---
# <a name="tb_getinsertmark-message"></a><span data-ttu-id="5f1c0-104">\_Mensaje GETINSERTMARK TB</span><span class="sxs-lookup"><span data-stu-id="5f1c0-104">TB\_GETINSERTMARK message</span></span>

<span data-ttu-id="5f1c0-105">Recupera la marca de inserción actual de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="5f1c0-105">Retrieves the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f1c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f1c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f1c0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f1c0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5f1c0-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f1c0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5f1c0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f1c0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f1c0-110">Puntero a una estructura [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) que recibe la marca de inserción.</span><span class="sxs-lookup"><span data-stu-id="5f1c0-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f1c0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f1c0-111">Return value</span></span>

<span data-ttu-id="5f1c0-112">Siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="5f1c0-112">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f1c0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f1c0-113">Requirements</span></span>



| <span data-ttu-id="5f1c0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f1c0-114">Requirement</span></span> | <span data-ttu-id="5f1c0-115">Value</span><span class="sxs-lookup"><span data-stu-id="5f1c0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f1c0-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f1c0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5f1c0-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5f1c0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f1c0-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f1c0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5f1c0-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f1c0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f1c0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f1c0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f1c0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f1c0-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f1c0-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f1c0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f1c0-123">**TB \_ SETINSERTMARK**</span><span class="sxs-lookup"><span data-stu-id="5f1c0-123">**TB\_SETINSERTMARK**</span></span>](tb-setinsertmark.md)
</dt> </dl>

 

 





