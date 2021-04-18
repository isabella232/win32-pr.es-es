---
title: Mensaje de TTM_HITTEST (commctrl. h)
description: Comprueba un punto para determinar si está dentro del rectángulo delimitador de la herramienta especificada y, si es así, recupera información sobre la herramienta.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- TTM_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_HITTEST
- TTM_HITTESTA
- TTM_HITTESTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b515ccb5c283b66760f24c02749368e424e6fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490673"
---
# <a name="ttm_hittest-message"></a><span data-ttu-id="7c852-104">TTM \_ mensaje HITTEST</span><span class="sxs-lookup"><span data-stu-id="7c852-104">TTM\_HITTEST message</span></span>

<span data-ttu-id="7c852-105">Comprueba un punto para determinar si está dentro del rectángulo delimitador de la herramienta especificada y, si es así, recupera información sobre la herramienta.</span><span class="sxs-lookup"><span data-stu-id="7c852-105">Tests a point to determine whether it is within the bounding rectangle of the specified tool and, if it is, retrieves information about the tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c852-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c852-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c852-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c852-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7c852-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7c852-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7c852-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c852-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c852-110">Puntero a una estructura [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) .</span><span class="sxs-lookup"><span data-stu-id="7c852-110">Pointer to a [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) structure.</span></span> <span data-ttu-id="7c852-111">Al enviar el mensaje, el miembro **hWnd** debe especificar el identificador de una herramienta y el miembro **PT** debe especificar las coordenadas de un punto.</span><span class="sxs-lookup"><span data-stu-id="7c852-111">When sending the message, the **hwnd** member must specify the handle to a tool and the **pt** member must specify the coordinates of a point.</span></span> <span data-ttu-id="7c852-112">Si el valor devuelto es **true**, el miembro de **ti** (una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ) recibe información sobre la herramienta que ocupa el punto.</span><span class="sxs-lookup"><span data-stu-id="7c852-112">If the return value is **TRUE**, the **ti** member (a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure) receives information about the tool that occupies the point.</span></span> <span data-ttu-id="7c852-113">El miembro **cbSize** de la estructura de **ti** se debe rellenar antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="7c852-113">The **cbSize** member of the **ti** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c852-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c852-114">Return value</span></span>

<span data-ttu-id="7c852-115">Devuelve **true** si la herramienta ocupa el punto especificado o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7c852-115">Returns **TRUE** if the tool occupies the specified point, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c852-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c852-116">Remarks</span></span>

<span data-ttu-id="7c852-117">Este mensaje se debe enviar cuando la herramienta tiene establecida la \_ marca de seguimiento ttf.</span><span class="sxs-lookup"><span data-stu-id="7c852-117">This message must be sent when the tool has the TTF\_TRACK flag set.</span></span> <span data-ttu-id="7c852-118">Para obtener más información sobre esta marca, vea [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa).</span><span class="sxs-lookup"><span data-stu-id="7c852-118">For more information on this flag, see [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa).</span></span> <span data-ttu-id="7c852-119">TTM \_ HITTEST producirá un error si \_ no se establece la pista ttf, independientemente de si el punto de acierto está en el rectángulo de herramientas o no.</span><span class="sxs-lookup"><span data-stu-id="7c852-119">TTM\_HITTEST will fail if TTF\_TRACK is not set, regardless if the hit point is in the tools rectangle or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c852-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c852-120">Requirements</span></span>



| <span data-ttu-id="7c852-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c852-121">Requirement</span></span> | <span data-ttu-id="7c852-122">Value</span><span class="sxs-lookup"><span data-stu-id="7c852-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c852-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c852-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7c852-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7c852-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c852-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c852-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7c852-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c852-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c852-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c852-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c852-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c852-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7c852-129">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="7c852-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7c852-130">**TTM \_ HITTESTW** (Unicode) y **TTM \_ HITTESTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7c852-130">**TTM\_HITTESTW** (Unicode) and **TTM\_HITTESTA** (ANSI)</span></span><br/>                   |



 

 





