---
title: Mensaje de LVM_SUBITEMHITTEST (commctrl. h)
description: Determina qué elemento o subelemento de vista de lista se encuentra en una posición determinada. Puede enviar este mensaje explícitamente o mediante la \_ macro SubItemHitTest de ListView.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- LVM_SUBITEMHITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489257"
---
# <a name="lvm_subitemhittest-message"></a><span data-ttu-id="2b842-105">\_Mensaje SUBITEMHITTEST LVM</span><span class="sxs-lookup"><span data-stu-id="2b842-105">LVM\_SUBITEMHITTEST message</span></span>

<span data-ttu-id="2b842-106">Determina qué elemento o subelemento de vista de lista se encuentra en una posición determinada.</span><span class="sxs-lookup"><span data-stu-id="2b842-106">Determines which list-view item or subitem is at a given position.</span></span> <span data-ttu-id="2b842-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SubItemHitTest de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) .</span><span class="sxs-lookup"><span data-stu-id="2b842-107">You can send this message explicitly or by using the [**ListView\_SubItemHitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b842-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b842-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b842-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b842-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2b842-110">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="2b842-110">Must be 0.</span></span> <span data-ttu-id="2b842-111">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="2b842-111">**Windows Vista.**</span></span> <span data-ttu-id="2b842-112">Debe ser-1 si se va a recuperar el miembro **iGroup** de *lParam* .</span><span class="sxs-lookup"><span data-stu-id="2b842-112">Should be -1 if the **iGroup** member of *lParam* is to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="2b842-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b842-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b842-114">Puntero a una estructura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="2b842-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure.</span></span> <span data-ttu-id="2b842-115">La estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) dentro de **LVHITTESTINFO** debe establecerse en las coordenadas de cliente en las que se va a realizar la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="2b842-115">The [**POINT**](/previous-versions//dd162805(v=vs.85)) structure within **LVHITTESTINFO** should be set to the client coordinates to be hit-tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b842-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b842-116">Return value</span></span>

<span data-ttu-id="2b842-117">Devuelve el índice del elemento o subelemento probado, si existe, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2b842-117">Returns the index of the item or subitem tested, if any, or -1 otherwise.</span></span> <span data-ttu-id="2b842-118">Si un elemento o subelemento está en las coordenadas especificadas, los campos de la estructura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) se rellenarán con la información de aciertos correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2b842-118">If an item or subitem is at the given coordinates, the fields of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure will be filled with the applicable hit information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b842-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b842-119">Requirements</span></span>



| <span data-ttu-id="2b842-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b842-120">Requirement</span></span> | <span data-ttu-id="2b842-121">Value</span><span class="sxs-lookup"><span data-stu-id="2b842-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b842-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b842-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2b842-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2b842-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b842-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b842-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2b842-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b842-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b842-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b842-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b842-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b842-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

