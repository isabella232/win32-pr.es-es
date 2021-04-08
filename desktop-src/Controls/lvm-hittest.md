---
title: Mensaje de LVM_HITTEST (commctrl. h)
description: Determina qué elemento de vista de lista, si existe, está en una posición especificada. Puede enviar este mensaje explícitamente o mediante la \_ macro HitTest de ListView.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- LVM_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb770c8f5a47f1dcbbf23a11443afa581aea2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996907"
---
# <a name="lvm_hittest-message"></a><span data-ttu-id="2c4e5-105">El \_ mensaje de LVM HITTEST</span><span class="sxs-lookup"><span data-stu-id="2c4e5-105">LVM\_HITTEST message</span></span>

<span data-ttu-id="2c4e5-106">Determina qué elemento de vista de lista, si existe, está en una posición especificada.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-106">Determines which list-view item, if any, is at a specified position.</span></span> <span data-ttu-id="2c4e5-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ HitTest de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) .</span><span class="sxs-lookup"><span data-stu-id="2c4e5-107">You can send this message explicitly or by using the [**ListView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c4e5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c4e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c4e5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c4e5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2c4e5-110">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-110">Must be 0.</span></span> <span data-ttu-id="2c4e5-111">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="2c4e5-111">**Windows Vista.**</span></span> <span data-ttu-id="2c4e5-112">Debe ser-1 si se van a recuperar los miembros **iGroup** y **iSubItem** de la estructura *lParam* .</span><span class="sxs-lookup"><span data-stu-id="2c4e5-112">Should be -1 if the **iGroup** and **iSubItem** members of the *lParam* structure are to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="2c4e5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c4e5-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c4e5-114">Puntero a una estructura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) que contiene la posición para la prueba de posicionamiento y recibe información sobre los resultados de la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure that contains the position to hit test and receives information about the results of the hit test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c4e5-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c4e5-115">Return value</span></span>

<span data-ttu-id="2c4e5-116">Devuelve el índice del elemento en la posición especificada, si existe, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2c4e5-116">Returns the index of the item at the specified position, if any, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c4e5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c4e5-117">Requirements</span></span>



| <span data-ttu-id="2c4e5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c4e5-118">Requirement</span></span> | <span data-ttu-id="2c4e5-119">Value</span><span class="sxs-lookup"><span data-stu-id="2c4e5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4e5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c4e5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2c4e5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2c4e5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c4e5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c4e5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2c4e5-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c4e5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c4e5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c4e5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c4e5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c4e5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





