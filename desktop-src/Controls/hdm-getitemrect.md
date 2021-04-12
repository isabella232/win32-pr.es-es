---
title: Mensaje de HDM_GETITEMRECT (commctrl. h)
description: Obtiene el rectángulo delimitador de un elemento determinado en un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header GetItemRect.
ms.assetid: b483ef97-3700-425b-8160-81c673850f68
keywords:
- HDM_GETITEMRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4baec72bd914a9d2dad72556a5444c0059452cf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491476"
---
# <a name="hdm_getitemrect-message"></a><span data-ttu-id="bc35c-105">HDM \_ GETITEMRECT</span><span class="sxs-lookup"><span data-stu-id="bc35c-105">HDM\_GETITEMRECT message</span></span>

<span data-ttu-id="bc35c-106">Obtiene el rectángulo delimitador de un elemento determinado en un control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="bc35c-106">Gets the bounding rectangle for a given item in a header control.</span></span> <span data-ttu-id="bc35c-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="bc35c-107">You can send this message explicitly or use the [**Header\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc35c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc35c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc35c-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc35c-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc35c-110">Índice de base cero del elemento de control de encabezado para el que se va a recuperar el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="bc35c-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="bc35c-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bc35c-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc35c-112">Puntero a una estructura [**Rect**](/windows/win32/api/windef/ns-windef-rect) que recibe la información del rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="bc35c-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="bc35c-113">El remitente del mensaje es responsable de la asignación de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="bc35c-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="bc35c-114">Las coordenadas devueltas en la estructura RECT se expresan en relación con el elemento primario del control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="bc35c-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc35c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc35c-115">Return value</span></span>

<span data-ttu-id="bc35c-116">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="bc35c-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc35c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc35c-117">Requirements</span></span>



| <span data-ttu-id="bc35c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc35c-118">Requirement</span></span> | <span data-ttu-id="bc35c-119">Value</span><span class="sxs-lookup"><span data-stu-id="bc35c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc35c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc35c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bc35c-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bc35c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc35c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc35c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bc35c-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc35c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc35c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc35c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc35c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc35c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





