---
title: Mensaje EM_SETTOUCHOPTIONS (RichEdit. h)
description: Establece las opciones de toque asociadas a un control Rich Edit.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- EM_SETTOUCHOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7613679a574955ef726da9fa10e8d919c8fe53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491200"
---
# <a name="em_settouchoptions-message"></a><span data-ttu-id="effd7-104">\_Mensaje SETTOUCHOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="effd7-104">EM\_SETTOUCHOPTIONS message</span></span>

<span data-ttu-id="effd7-105">Establece las opciones de toque asociadas a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="effd7-105">Sets the touch options associated with a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="effd7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="effd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="effd7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="effd7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="effd7-108">Opción de toque que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="effd7-108">The touch option to set.</span></span> <span data-ttu-id="effd7-109">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="effd7-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="effd7-110">Valor</span><span class="sxs-lookup"><span data-stu-id="effd7-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="effd7-111">Significado</span><span class="sxs-lookup"><span data-stu-id="effd7-111">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="effd7-112"><dt>**RTO \_ SHOWHANDLES**</dt></span><span class="sxs-lookup"><span data-stu-id="effd7-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="effd7-113">Mostrar u ocultar los controladores de la agarrador táctil, dependiendo del valor de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="effd7-113">Show or hide the touch gripper handles, depending on the value of *lParam*.</span></span><br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="effd7-114"><dt>**RTO \_ DISABLEHANDLES**</dt></span><span class="sxs-lookup"><span data-stu-id="effd7-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="effd7-115">Habilitar o deshabilitar los identificadores de la agarración táctil, dependiendo del valor de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="effd7-115">Enable or disable the touch gripper handles, depending on the value of *lParam*.</span></span> <span data-ttu-id="effd7-116">Cuando se deshabilitan los identificadores, se ocultan si están visibles y permanecen ocultos hasta que un mensaje **\_ SETTOUCHOPTIONS em** cambia su estado.</span><span class="sxs-lookup"><span data-stu-id="effd7-116">When handles are disabled, they are hidden if they are visible and remain hidden until an **EM\_SETTOUCHOPTIONS** message changes their status.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="effd7-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="effd7-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="effd7-118">Establézcalo en **true** para mostrar/habilitar los manipuladores de la selección táctil, o en **false** para ocultar o deshabilitar los controladores de selección táctil.</span><span class="sxs-lookup"><span data-stu-id="effd7-118">Set to **TRUE** to show/enable the touch selection handles, or **FALSE** to hide/disable the touch selection handles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="effd7-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="effd7-119">Return value</span></span>

<span data-ttu-id="effd7-120">Este mensaje devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="effd7-120">This message returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="effd7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="effd7-121">Requirements</span></span>



| <span data-ttu-id="effd7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="effd7-122">Requirement</span></span> | <span data-ttu-id="effd7-123">Value</span><span class="sxs-lookup"><span data-stu-id="effd7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="effd7-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="effd7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="effd7-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="effd7-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="effd7-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="effd7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="effd7-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="effd7-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="effd7-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="effd7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="effd7-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="effd7-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="effd7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="effd7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="effd7-131">**\_GETTOUCHOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="effd7-131">**EM\_GETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 





