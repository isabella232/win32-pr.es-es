---
title: Mensaje de LVM_FINDITEM (commctrl. h)
description: Busca un elemento de vista de lista con las características especificadas. Puede enviar este mensaje explícitamente o mediante la macro de ListView \_ FindItem.
ms.assetid: 3b18c8ad-97e6-4f4d-bf89-afb95f925ed1
keywords:
- LVM_FINDITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_FINDITEM
- LVM_FINDITEMA
- LVM_FINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f7dfc19e263a6ab7ad29b5e514fa4e52c1a9ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489077"
---
# <a name="lvm_finditem-message"></a><span data-ttu-id="1206d-105">\_Mensaje FINDITEM LVM</span><span class="sxs-lookup"><span data-stu-id="1206d-105">LVM\_FINDITEM message</span></span>

<span data-ttu-id="1206d-106">Busca un elemento de vista de lista con las características especificadas.</span><span class="sxs-lookup"><span data-stu-id="1206d-106">Searches for a list-view item with the specified characteristics.</span></span> <span data-ttu-id="1206d-107">Puede enviar este mensaje explícitamente o mediante la macro de [**ListView \_ FindItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) .</span><span class="sxs-lookup"><span data-stu-id="1206d-107">You can send this message explicitly or by using the [**ListView\_FindItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1206d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1206d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1206d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1206d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1206d-110">Índice del elemento en el que se va a comenzar la búsqueda o-1 para empezar desde el principio.</span><span class="sxs-lookup"><span data-stu-id="1206d-110">The index of the item to begin the search with or -1 to start from the beginning.</span></span> <span data-ttu-id="1206d-111">El elemento especificado se excluye de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1206d-111">The specified item is itself excluded from the search.</span></span>

</dd> <dt>

<span data-ttu-id="1206d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1206d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1206d-113">Puntero a una estructura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) que contiene información sobre lo que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="1206d-113">A pointer to an [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure that contains information about what to search for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1206d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1206d-114">Return value</span></span>

<span data-ttu-id="1206d-115">Devuelve el índice del elemento si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1206d-115">Returns the index of the item if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1206d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1206d-116">Requirements</span></span>



| <span data-ttu-id="1206d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1206d-117">Requirement</span></span> | <span data-ttu-id="1206d-118">Value</span><span class="sxs-lookup"><span data-stu-id="1206d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1206d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1206d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1206d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1206d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1206d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1206d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1206d-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1206d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1206d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1206d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1206d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1206d-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1206d-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1206d-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1206d-126">**LVM \_ FINDITEMW** (Unicode) y **\_ FINDITEMA de LVM** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1206d-126">**LVM\_FINDITEMW** (Unicode) and **LVM\_FINDITEMA** (ANSI)</span></span><br/>                 |



 

 





