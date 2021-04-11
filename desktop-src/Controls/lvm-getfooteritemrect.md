---
title: Mensaje de LVM_GETFOOTERITEMRECT (commctrl. h)
description: Obtiene las coordenadas de un pie de página para un elemento especificado en un control de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro GetFooterItemRect de ListView.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- LVM_GETFOOTERITEMRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142cb92806fa1d58faa0414c10c41bd2815d5b6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274508"
---
# <a name="lvm_getfooteritemrect-message"></a><span data-ttu-id="56ff9-105">\_Mensaje GETFOOTERITEMRECT LVM</span><span class="sxs-lookup"><span data-stu-id="56ff9-105">LVM\_GETFOOTERITEMRECT message</span></span>

<span data-ttu-id="56ff9-106">Obtiene las coordenadas de un pie de página para un elemento especificado en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="56ff9-106">Gets the coordinates of a footer for a specified item in a list-view control.</span></span> <span data-ttu-id="56ff9-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetFooterItemRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) .</span><span class="sxs-lookup"><span data-stu-id="56ff9-107">Send this message explicitly or by using the [**ListView\_GetFooterItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="56ff9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56ff9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56ff9-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="56ff9-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56ff9-110">Índice del elemento en el control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="56ff9-110">The index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="56ff9-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="56ff9-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="56ff9-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para recibir las coordenadas.</span><span class="sxs-lookup"><span data-stu-id="56ff9-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="56ff9-113">La aplicación que realiza la llamada es responsable de la asignación de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="56ff9-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="56ff9-114">Las coordenadas recibidas se expresan como coordenadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="56ff9-114">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56ff9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56ff9-115">Return value</span></span>

<span data-ttu-id="56ff9-116">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="56ff9-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="56ff9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56ff9-117">Requirements</span></span>



| <span data-ttu-id="56ff9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="56ff9-118">Requirement</span></span> | <span data-ttu-id="56ff9-119">Value</span><span class="sxs-lookup"><span data-stu-id="56ff9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56ff9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56ff9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="56ff9-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="56ff9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56ff9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56ff9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="56ff9-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="56ff9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56ff9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56ff9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="56ff9-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56ff9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

