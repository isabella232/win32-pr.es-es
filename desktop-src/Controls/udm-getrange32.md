---
title: Mensaje de UDM_GETRANGE32 (commctrl. h)
description: Recupera el intervalo de 32 bits de un control de flechas.
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- UDM_GETRANGE32 controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca418cd08dc4c81b3ff734d74f3ca9deeef7d848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490181"
---
# <a name="udm_getrange32-message"></a><span data-ttu-id="cc834-104">\_Mensaje GETRANGE32 UDM</span><span class="sxs-lookup"><span data-stu-id="cc834-104">UDM\_GETRANGE32 message</span></span>

<span data-ttu-id="cc834-105">Recupera el intervalo de 32 bits de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="cc834-105">Retrieves the 32-bit range of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc834-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc834-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc834-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc834-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc834-108">Puntero a un entero con signo que recibe el límite inferior del intervalo de control de flechas.</span><span class="sxs-lookup"><span data-stu-id="cc834-108">Pointer to a signed integer that receives the lower limit of the up-down control range.</span></span> <span data-ttu-id="cc834-109">Este parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="cc834-109">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc834-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc834-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc834-111">Puntero a un entero con signo que recibe el límite superior del intervalo de control de flechas.</span><span class="sxs-lookup"><span data-stu-id="cc834-111">Pointer to a signed integer that receives the upper limit of the up-down control range.</span></span> <span data-ttu-id="cc834-112">Este parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="cc834-112">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc834-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc834-113">Return value</span></span>

<span data-ttu-id="cc834-114">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="cc834-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc834-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc834-115">Requirements</span></span>



| <span data-ttu-id="cc834-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc834-116">Requirement</span></span> | <span data-ttu-id="cc834-117">Value</span><span class="sxs-lookup"><span data-stu-id="cc834-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc834-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc834-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cc834-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cc834-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc834-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc834-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cc834-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc834-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc834-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc834-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc834-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc834-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





