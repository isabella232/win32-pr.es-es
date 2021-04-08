---
title: Mensaje de RB_SETPALETTE (commctrl. h)
description: Establece la paleta actual del control rebar.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- RB_SETPALETTE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996721"
---
# <a name="rb_setpalette-message"></a><span data-ttu-id="eabda-104">Mensaje de SETPALETTE de RB \_</span><span class="sxs-lookup"><span data-stu-id="eabda-104">RB\_SETPALETTE message</span></span>

<span data-ttu-id="eabda-105">Establece la paleta actual del control rebar.</span><span class="sxs-lookup"><span data-stu-id="eabda-105">Sets the rebar control's current palette.</span></span>

## <a name="parameters"></a><span data-ttu-id="eabda-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eabda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eabda-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eabda-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eabda-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="eabda-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eabda-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eabda-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eabda-110">**HPALETTE** que especifica la nueva paleta que usará el control rebar.</span><span class="sxs-lookup"><span data-stu-id="eabda-110">An **HPALETTE** that specifies the new palette that the rebar control will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eabda-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eabda-111">Return value</span></span>

<span data-ttu-id="eabda-112">Devuelve un **HPALETTE** que especifica la paleta anterior del control rebar.</span><span class="sxs-lookup"><span data-stu-id="eabda-112">Returns an **HPALETTE** that specifies the rebar control's previous palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="eabda-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eabda-113">Remarks</span></span>

<span data-ttu-id="eabda-114">Es responsabilidad de la aplicación que envía este mensaje eliminar el **HPALETTE** que se pasa en este mensaje (vea [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)).</span><span class="sxs-lookup"><span data-stu-id="eabda-114">It is the responsibility of the application sending this message to delete the **HPALETTE** passed in this message (see [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)).</span></span> <span data-ttu-id="eabda-115">El control rebar no eliminará un conjunto de **HPALETTE** con este mensaje.</span><span class="sxs-lookup"><span data-stu-id="eabda-115">The rebar control will not delete an **HPALETTE** set with this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="eabda-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eabda-116">Requirements</span></span>



| <span data-ttu-id="eabda-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="eabda-117">Requirement</span></span> | <span data-ttu-id="eabda-118">Value</span><span class="sxs-lookup"><span data-stu-id="eabda-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eabda-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eabda-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eabda-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eabda-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eabda-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eabda-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eabda-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="eabda-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eabda-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eabda-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eabda-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eabda-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eabda-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="eabda-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eabda-126">**\_GETPALETTE RB**</span><span class="sxs-lookup"><span data-stu-id="eabda-126">**RB\_GETPALETTE**</span></span>](rb-getpalette.md)
</dt> </dl>

 

