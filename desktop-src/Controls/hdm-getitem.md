---
title: Mensaje de HDM_GETITEM (commctrl. h)
description: Obtiene información sobre un elemento de un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetItem de encabezado.
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- HDM_GETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2073602121480930e0f7d9d2e5a904c0dea77ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150318"
---
# <a name="hdm_getitem-message"></a><span data-ttu-id="4ba42-105">HDM \_ mensaje GETITEM</span><span class="sxs-lookup"><span data-stu-id="4ba42-105">HDM\_GETITEM message</span></span>

<span data-ttu-id="4ba42-106">Obtiene información sobre un elemento de un control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="4ba42-106">Gets information about an item in a header control.</span></span> <span data-ttu-id="4ba42-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetItem de encabezado**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) .</span><span class="sxs-lookup"><span data-stu-id="4ba42-107">You can send this message explicitly or use the [**Header\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ba42-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ba42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ba42-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ba42-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ba42-110">Índice del elemento para el que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="4ba42-110">The index of the item for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="4ba42-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ba42-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ba42-112">Puntero a una estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) .</span><span class="sxs-lookup"><span data-stu-id="4ba42-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="4ba42-113">Cuando se envía el mensaje, el miembro de la **máscara** indica el tipo de información que se solicita.</span><span class="sxs-lookup"><span data-stu-id="4ba42-113">When the message is sent, the **mask** member indicates the type of information being requested.</span></span> <span data-ttu-id="4ba42-114">Cuando el mensaje vuelve, los demás miembros reciben la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="4ba42-114">When the message returns, the other members receive the requested information.</span></span> <span data-ttu-id="4ba42-115">Si el miembro de la **máscara** especifica cero, el mensaje devuelve **true** pero no copia ninguna información en la estructura.</span><span class="sxs-lookup"><span data-stu-id="4ba42-115">If the **mask** member specifies zero, the message returns **TRUE** but copies no information to the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ba42-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ba42-116">Return value</span></span>

<span data-ttu-id="4ba42-117">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4ba42-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ba42-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ba42-118">Remarks</span></span>

<span data-ttu-id="4ba42-119">Si la \_ marca de texto HDI se establece en el miembro **Mask** de la estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) , el control puede cambiar el miembro **miembros pszText** de la estructura para que apunte al nuevo texto en lugar de llenar el búfer con el texto solicitado.</span><span class="sxs-lookup"><span data-stu-id="4ba42-119">If the HDI\_TEXT flag is set in the **mask** member of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="4ba42-120">Las aplicaciones no deben suponer que el texto siempre se colocará en el búfer solicitado.</span><span class="sxs-lookup"><span data-stu-id="4ba42-120">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ba42-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ba42-121">Requirements</span></span>



| <span data-ttu-id="4ba42-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ba42-122">Requirement</span></span> | <span data-ttu-id="4ba42-123">Value</span><span class="sxs-lookup"><span data-stu-id="4ba42-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ba42-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ba42-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4ba42-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4ba42-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4ba42-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ba42-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4ba42-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4ba42-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ba42-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ba42-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ba42-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ba42-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4ba42-130">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="4ba42-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4ba42-131">**HDM \_ GETITEMW** (Unicode) y **HDM \_ GETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4ba42-131">**HDM\_GETITEMW** (Unicode) and **HDM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





