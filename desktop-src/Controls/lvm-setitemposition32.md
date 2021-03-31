---
title: Mensaje de LVM_SETITEMPOSITION32 (commctrl. h)
description: Mueve un elemento a una posición especificada en un control de vista de lista (debe estar en el icono o en la vista de iconos pequeños).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- LVM_SETITEMPOSITION32 controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079430"
---
# <a name="lvm_setitemposition32-message"></a><span data-ttu-id="e1ced-104">\_Mensaje SETITEMPOSITION32 LVM</span><span class="sxs-lookup"><span data-stu-id="e1ced-104">LVM\_SETITEMPOSITION32 message</span></span>

<span data-ttu-id="e1ced-105">Mueve un elemento a una posición especificada en un control de vista de lista (debe estar en el icono o en la vista de iconos pequeños).</span><span class="sxs-lookup"><span data-stu-id="e1ced-105">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="e1ced-106">Este mensaje difiere del mensaje [**\_ SETITEMPOSITION LVM**](lvm-setitemposition.md) en que usa coordenadas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e1ced-106">This message differs from the [**LVM\_SETITEMPOSITION**](lvm-setitemposition.md) message in that it uses 32-bit coordinates.</span></span> <span data-ttu-id="e1ced-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItemPosition32 de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) .</span><span class="sxs-lookup"><span data-stu-id="e1ced-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1ced-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1ced-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1ced-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1ced-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1ced-110">Índice del elemento de vista de lista para el que se va a establecer la posición.</span><span class="sxs-lookup"><span data-stu-id="e1ced-110">Index of the list-view item for which to set the position.</span></span>

</dd> <dt>

<span data-ttu-id="e1ced-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1ced-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1ced-112">Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que contiene la nueva posición del elemento, en coordenadas de la vista de lista.</span><span class="sxs-lookup"><span data-stu-id="e1ced-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the new position of the item, in list-view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1ced-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1ced-113">Return value</span></span>

<span data-ttu-id="e1ced-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e1ced-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1ced-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1ced-115">Requirements</span></span>



| <span data-ttu-id="e1ced-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1ced-116">Requirement</span></span> | <span data-ttu-id="e1ced-117">Value</span><span class="sxs-lookup"><span data-stu-id="e1ced-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ced-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1ced-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e1ced-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e1ced-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1ced-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1ced-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e1ced-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1ced-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1ced-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1ced-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1ced-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1ced-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

