---
title: Mensaje de UDM_SETACCEL (commctrl. h)
description: Establece la aceleración para un control de flechas.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- UDM_SETACCEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43ed290ce1668ffcaa9fb086a99ad52e5129ad6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079769"
---
# <a name="udm_setaccel-message"></a><span data-ttu-id="b5838-104">\_Mensaje SETACCEL UDM</span><span class="sxs-lookup"><span data-stu-id="b5838-104">UDM\_SETACCEL message</span></span>

<span data-ttu-id="b5838-105">Establece la aceleración para un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="b5838-105">Sets the acceleration for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5838-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5838-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5838-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5838-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5838-108">Número de estructuras [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) especificadas por *aAccels*.</span><span class="sxs-lookup"><span data-stu-id="b5838-108">Number of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures specified by *aAccels*.</span></span>

</dd> <dt>

<span data-ttu-id="b5838-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5838-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5838-110">Puntero a una matriz de estructuras [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) que contienen información de aceleración.</span><span class="sxs-lookup"><span data-stu-id="b5838-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that contain acceleration information.</span></span> <span data-ttu-id="b5838-111">Los elementos deben ordenarse en orden ascendente según el miembro **nSec** .</span><span class="sxs-lookup"><span data-stu-id="b5838-111">Elements should be sorted in ascending order based on the **nSec** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5838-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5838-112">Return value</span></span>

<span data-ttu-id="b5838-113">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b5838-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5838-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5838-114">Requirements</span></span>



| <span data-ttu-id="b5838-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5838-115">Requirement</span></span> | <span data-ttu-id="b5838-116">Value</span><span class="sxs-lookup"><span data-stu-id="b5838-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5838-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5838-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b5838-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b5838-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5838-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5838-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b5838-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5838-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5838-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5838-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5838-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5838-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5838-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5838-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5838-124">**UDM \_ GETACCEL**</span><span class="sxs-lookup"><span data-stu-id="b5838-124">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)
</dt> </dl>

 

 





