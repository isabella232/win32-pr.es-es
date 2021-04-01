---
title: Mensaje de MCM_GETCALENDARGRIDINFO (commctrl. h)
description: Obtiene información acerca de una cuadrícula de calendario.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- MCM_GETCALENDARGRIDINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506f6193ab32d059bb85fa4583441bfbe027f224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804147"
---
# <a name="mcm_getcalendargridinfo-message"></a><span data-ttu-id="116ed-104">Mensaje de MCM \_ GETCALENDARGRIDINFO</span><span class="sxs-lookup"><span data-stu-id="116ed-104">MCM\_GETCALENDARGRIDINFO message</span></span>

<span data-ttu-id="116ed-105">Obtiene información acerca de una cuadrícula de calendario.</span><span class="sxs-lookup"><span data-stu-id="116ed-105">Gets information about a calendar grid.</span></span>

## <a name="parameters"></a><span data-ttu-id="116ed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="116ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="116ed-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="116ed-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="116ed-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="116ed-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="116ed-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="116ed-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="116ed-110">Puntero a una estructura [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) que contiene información sobre la cuadrícula del calendario.</span><span class="sxs-lookup"><span data-stu-id="116ed-110">Pointer to an [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) structure that contains information about the calendar grid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="116ed-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="116ed-111">Return value</span></span>

<span data-ttu-id="116ed-112">**True** si es correcto; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="116ed-112">**TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="116ed-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="116ed-113">Requirements</span></span>



| <span data-ttu-id="116ed-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="116ed-114">Requirement</span></span> | <span data-ttu-id="116ed-115">Value</span><span class="sxs-lookup"><span data-stu-id="116ed-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="116ed-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="116ed-116">Minimum supported client</span></span><br/> | <span data-ttu-id="116ed-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="116ed-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="116ed-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="116ed-118">Minimum supported server</span></span><br/> | <span data-ttu-id="116ed-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="116ed-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="116ed-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="116ed-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="116ed-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="116ed-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





