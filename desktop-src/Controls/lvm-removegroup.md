---
title: Mensaje de LVM_REMOVEGROUP (commctrl. h)
description: Quita un grupo de un control de vista de lista.
ms.assetid: c6f4f54c-4cf8-47d0-8e96-fa8a1df0501b
keywords:
- LVM_REMOVEGROUP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_REMOVEGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa631593e791f90c76a9f74aa1d967d9678540f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996645"
---
# <a name="lvm_removegroup-message"></a><span data-ttu-id="679cf-104">\_Mensaje REMOVEGROUP LVM</span><span class="sxs-lookup"><span data-stu-id="679cf-104">LVM\_REMOVEGROUP message</span></span>

<span data-ttu-id="679cf-105">Quita un grupo de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="679cf-105">Removes a group from a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="679cf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="679cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="679cf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="679cf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="679cf-108">IDENTIFICADOR que especifica el grupo que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="679cf-108">ID that specifies the group to remove.</span></span></dd> <dt>

<span data-ttu-id="679cf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="679cf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="679cf-110">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="679cf-110">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="679cf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="679cf-111">Return value</span></span>

<span data-ttu-id="679cf-112">Devuelve el índice del grupo si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="679cf-112">Returns the index of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="679cf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="679cf-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="679cf-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="679cf-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="679cf-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="679cf-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="679cf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="679cf-116">Requirements</span></span>



| <span data-ttu-id="679cf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="679cf-117">Requirement</span></span> | <span data-ttu-id="679cf-118">Value</span><span class="sxs-lookup"><span data-stu-id="679cf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="679cf-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="679cf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="679cf-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="679cf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="679cf-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="679cf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="679cf-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="679cf-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="679cf-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="679cf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="679cf-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="679cf-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





