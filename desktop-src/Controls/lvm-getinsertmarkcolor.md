---
title: Mensaje de LVM_GETINSERTMARKCOLOR (commctrl. h)
description: Recupera el color del punto de inserción.
ms.assetid: 1e98023a-9d26-4b87-bee4-bee4939ccfca
keywords:
- LVM_GETINSERTMARKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18d6e9ed277f447f5097c0954819029d24b9cbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151285"
---
# <a name="lvm_getinsertmarkcolor-message"></a><span data-ttu-id="e8151-104">\_Mensaje GETINSERTMARKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="e8151-104">LVM\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="e8151-105">Recupera el color del punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="e8151-105">Retrieves the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8151-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8151-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8151-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8151-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e8151-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e8151-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e8151-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8151-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e8151-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e8151-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8151-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8151-111">Return value</span></span>

<span data-ttu-id="e8151-112">Devuelve una estructura **COLORREF** que contiene el color del punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="e8151-112">Returns a **COLORREF** structure that contains the color of the insertion point.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8151-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8151-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8151-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="e8151-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e8151-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e8151-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8151-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8151-116">Requirements</span></span>



| <span data-ttu-id="e8151-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8151-117">Requirement</span></span> | <span data-ttu-id="e8151-118">Value</span><span class="sxs-lookup"><span data-stu-id="e8151-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8151-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8151-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e8151-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e8151-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8151-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8151-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e8151-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8151-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8151-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8151-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8151-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8151-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





