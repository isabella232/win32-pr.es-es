---
title: Mensaje de LVM_INSERTGROUP (commctrl. h)
description: Inserta un grupo en un control de vista de lista.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- LVM_INSERTGROUP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dbae780f7de26a5c791477e1a7321794054056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658332"
---
# <a name="lvm_insertgroup-message"></a><span data-ttu-id="65656-104">\_Mensaje INSERTGROUP LVM</span><span class="sxs-lookup"><span data-stu-id="65656-104">LVM\_INSERTGROUP message</span></span>

<span data-ttu-id="65656-105">Inserta un grupo en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="65656-105">Inserts a group into a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="65656-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65656-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65656-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65656-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="65656-108">Índice en el que se va a agregar el grupo.</span><span class="sxs-lookup"><span data-stu-id="65656-108">Index where the group is to be added.</span></span> <span data-ttu-id="65656-109">Si es-1, el grupo se agrega al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="65656-109">If this is -1, the group is added at the end of the list.</span></span></dd> <dt>

<span data-ttu-id="65656-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65656-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="65656-111">Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> que contiene el grupo que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="65656-111">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that contains the group to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65656-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65656-112">Return value</span></span>

<span data-ttu-id="65656-113">Devuelve el índice del elemento al que se agregó el grupo o-1 si se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="65656-113">Returns the index of the item that the group was added to, or -1 if the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="65656-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65656-114">Remarks</span></span>

<span data-ttu-id="65656-115">Para activar el modo de grupo, llame a [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) o [**ListView \_ ENABLEGROUPVIEW**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).</span><span class="sxs-lookup"><span data-stu-id="65656-115">To turn on group mode, call [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) or [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).</span></span>

<span data-ttu-id="65656-116">No se puede insertar un grupo en un control de vista de lista vacío.</span><span class="sxs-lookup"><span data-stu-id="65656-116">A group cannot be inserted into an empty list-view control.</span></span>

<span data-ttu-id="65656-117">Asegúrese de establecer el valor de **iGroupId** en los elementos a los que se agregó el grupo.</span><span class="sxs-lookup"><span data-stu-id="65656-117">Be sure to set the **iGroupId** in the item(s) the group was added to.</span></span> <span data-ttu-id="65656-118">De lo contrario, después del procesamiento de mensajes [**\_ ENABLEGROUPVIEW LVM**](lvm-enablegroupview.md) con **true** , el control ListView no mostrará ningún elemento.</span><span class="sxs-lookup"><span data-stu-id="65656-118">Otherwise after [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) message processing with **TRUE** the listview control will not show any items.</span></span>

> [!Note]  
> <span data-ttu-id="65656-119">Para usar este mensaje, debe proporcionar un manifiesto que especifique la versión 6,0 de Comclt32.</span><span class="sxs-lookup"><span data-stu-id="65656-119">To use this message, you must provide a manifest specifying Comclt32 version 6.0.</span></span> <span data-ttu-id="65656-120">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="65656-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65656-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65656-121">Requirements</span></span>



| <span data-ttu-id="65656-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="65656-122">Requirement</span></span> | <span data-ttu-id="65656-123">Value</span><span class="sxs-lookup"><span data-stu-id="65656-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65656-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65656-124">Minimum supported client</span></span><br/> | <span data-ttu-id="65656-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="65656-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65656-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65656-126">Minimum supported server</span></span><br/> | <span data-ttu-id="65656-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="65656-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65656-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65656-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="65656-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="65656-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





