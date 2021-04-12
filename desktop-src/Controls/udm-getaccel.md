---
title: Mensaje de UDM_GETACCEL (commctrl. h)
description: Recupera información de aceleración de un control de flechas.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- UDM_GETACCEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86a9740e59631b737453763a10ccb9820056d95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489628"
---
# <a name="udm_getaccel-message"></a><span data-ttu-id="d5f4f-104">\_Mensaje GETACCEL UDM</span><span class="sxs-lookup"><span data-stu-id="d5f4f-104">UDM\_GETACCEL message</span></span>

<span data-ttu-id="d5f4f-105">Recupera información de aceleración de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-105">Retrieves acceleration information for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5f4f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5f4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5f4f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5f4f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f4f-108">Número de elementos de la matriz especificada por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-108">Number of elements in the array specified by *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f4f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5f4f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f4f-110">Puntero a una matriz de estructuras [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) que reciben información de aceleración.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that receive acceleration information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5f4f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5f4f-111">Return value</span></span>

<span data-ttu-id="d5f4f-112">El valor devuelto es el número de aceleradores establecidos actualmente para el control.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-112">The return value is the number of accelerators currently set for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5f4f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5f4f-113">Requirements</span></span>



| <span data-ttu-id="d5f4f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5f4f-114">Requirement</span></span> | <span data-ttu-id="d5f4f-115">Value</span><span class="sxs-lookup"><span data-stu-id="d5f4f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f4f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5f4f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f4f-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d5f4f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5f4f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5f4f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f4f-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5f4f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5f4f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5f4f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f4f-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5f4f-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f4f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5f4f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f4f-123">**UDM \_ SETACCEL**</span><span class="sxs-lookup"><span data-stu-id="d5f4f-123">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)
</dt> </dl>

 

 





