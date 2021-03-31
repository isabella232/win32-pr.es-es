---
title: Mensaje de LVM_DELETECOLUMN (commctrl. h)
description: Quita una columna de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro DeleteColumn de ListView.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- LVM_DELETECOLUMN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa9005009ceaf42a01ede4f0f26334ae686c2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801129"
---
# <a name="lvm_deletecolumn-message"></a><span data-ttu-id="df189-105">\_Mensaje DELETECOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="df189-105">LVM\_DELETECOLUMN message</span></span>

<span data-ttu-id="df189-106">Quita una columna de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="df189-106">Removes a column from a list-view control.</span></span> <span data-ttu-id="df189-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ DeleteColumn de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) .</span><span class="sxs-lookup"><span data-stu-id="df189-107">You can send this message explicitly or by using the [**ListView\_DeleteColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="df189-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df189-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df189-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df189-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df189-110">Índice de la columna que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="df189-110">The index of the column to delete.</span></span>

</dd> <dt>

<span data-ttu-id="df189-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df189-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="df189-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="df189-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df189-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df189-113">Return value</span></span>

<span data-ttu-id="df189-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="df189-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="df189-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df189-115">Remarks</span></span>

<span data-ttu-id="df189-116">La eliminación de la columna cero de un control de vista de lista solo se admite en ComCtl32.dll versión 6 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="df189-116">Deleting column zero of a list-view control is supported only in ComCtl32.dll version 6 and later.</span></span> <span data-ttu-id="df189-117">La versión 5 también admite la eliminación de la columna cero, pero solo después de usar [**CCM \_ SETVERSION**](ccm-setversion.md) para establecer la versión en 5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="df189-117">Version 5 also supports deleting column zero, but only after you use [**CCM\_SETVERSION**](ccm-setversion.md) to set the version to 5 or later.</span></span> <span data-ttu-id="df189-118">En versiones anteriores a la versión 5, si tiene que eliminar la columna cero, inserte una columna ficticia de longitud cero cero y elimine la columna uno y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="df189-118">In versions prior to version 5, if you must delete column zero, insert a zero length dummy column zero and delete column one and above.</span></span>

## <a name="requirements"></a><span data-ttu-id="df189-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df189-119">Requirements</span></span>



| <span data-ttu-id="df189-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="df189-120">Requirement</span></span> | <span data-ttu-id="df189-121">Value</span><span class="sxs-lookup"><span data-stu-id="df189-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df189-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df189-122">Minimum supported client</span></span><br/> | <span data-ttu-id="df189-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="df189-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df189-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df189-124">Minimum supported server</span></span><br/> | <span data-ttu-id="df189-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="df189-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df189-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df189-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="df189-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="df189-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





