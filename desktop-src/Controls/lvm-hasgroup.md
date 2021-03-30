---
title: Mensaje de LVM_HASGROUP (commctrl. h)
description: Determina si el control de vista de lista tiene un grupo especificado.
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- LVM_HASGROUP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_HASGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb05fed8466188aa0025d2128ce64ad7f1512c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492394"
---
# <a name="lvm_hasgroup-message"></a><span data-ttu-id="91857-104">\_Mensaje HASGROUP LVM</span><span class="sxs-lookup"><span data-stu-id="91857-104">LVM\_HASGROUP message</span></span>

<span data-ttu-id="91857-105">Determina si el control de vista de lista tiene un grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="91857-105">Determines whether the list-view control has a specified group.</span></span>

## <a name="parameters"></a><span data-ttu-id="91857-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91857-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91857-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91857-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="91857-108">IDENTIFICADOR del grupo.</span><span class="sxs-lookup"><span data-stu-id="91857-108">ID of the group.</span></span></dd> <dt>

<span data-ttu-id="91857-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91857-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="91857-110">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="91857-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91857-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91857-111">Return value</span></span>

<span data-ttu-id="91857-112">Devuelve **true** si el control de vista de lista tiene el grupo especificado o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="91857-112">Returns **TRUE** if the list-view control has the specified group, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="91857-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91857-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="91857-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="91857-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="91857-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="91857-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="91857-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91857-116">Requirements</span></span>



| <span data-ttu-id="91857-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="91857-117">Requirement</span></span> | <span data-ttu-id="91857-118">Value</span><span class="sxs-lookup"><span data-stu-id="91857-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91857-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91857-119">Minimum supported client</span></span><br/> | <span data-ttu-id="91857-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="91857-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91857-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91857-121">Minimum supported server</span></span><br/> | <span data-ttu-id="91857-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="91857-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91857-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91857-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="91857-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91857-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





