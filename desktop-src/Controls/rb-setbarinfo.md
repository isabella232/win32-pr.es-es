---
title: Mensaje de RB_SETBARINFO (commctrl. h)
description: Establece las características de un control rebar.
ms.assetid: e4413d46-574f-4ccd-b5fd-3ba6c1e3924b
keywords:
- RB_SETBARINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_SETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b360bc0b4d14963619aad8f769634d7dd0ad17e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078926"
---
# <a name="rb_setbarinfo-message"></a><span data-ttu-id="a8346-104">Mensaje de SETBARINFO de RB \_</span><span class="sxs-lookup"><span data-stu-id="a8346-104">RB\_SETBARINFO message</span></span>

<span data-ttu-id="a8346-105">Establece las características de un control rebar.</span><span class="sxs-lookup"><span data-stu-id="a8346-105">Sets the characteristics of a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8346-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8346-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8346-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8346-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a8346-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a8346-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a8346-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8346-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8346-110">Puntero a una estructura [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) que contiene la información que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="a8346-110">Pointer to a [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) structure that contains the information to be set.</span></span> <span data-ttu-id="a8346-111">Debe establecer el miembro **cbSize** de esta estructura en **sizeof**(REBARINFO) antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="a8346-111">You must set the **cbSize** member of this structure to **sizeof**(REBARINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8346-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8346-112">Return value</span></span>

<span data-ttu-id="a8346-113">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="a8346-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8346-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8346-114">Requirements</span></span>



| <span data-ttu-id="a8346-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8346-115">Requirement</span></span> | <span data-ttu-id="a8346-116">Value</span><span class="sxs-lookup"><span data-stu-id="a8346-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8346-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8346-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8346-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a8346-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8346-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8346-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8346-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8346-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8346-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8346-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8346-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8346-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





