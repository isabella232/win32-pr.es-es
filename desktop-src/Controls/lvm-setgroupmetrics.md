---
title: Mensaje de LVM_SETGROUPMETRICS (commctrl. h)
description: Establece información sobre la presentación de grupos.
ms.assetid: 268b478d-da1f-4efe-9ee9-af3f12e089ee
keywords:
- LVM_SETGROUPMETRICS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8215962e6f84aac83a2151b46f489938b575303c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359668"
---
# <a name="lvm_setgroupmetrics-message"></a><span data-ttu-id="4505d-104">\_Mensaje SETGROUPMETRICS LVM</span><span class="sxs-lookup"><span data-stu-id="4505d-104">LVM\_SETGROUPMETRICS message</span></span>

<span data-ttu-id="4505d-105">Establece información sobre la presentación de grupos.</span><span class="sxs-lookup"><span data-stu-id="4505d-105">Sets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="4505d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4505d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4505d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4505d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4505d-108">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="4505d-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="4505d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4505d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4505d-110">Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> que contiene las métricas que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="4505d-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that contains the metrics to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4505d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4505d-111">Return value</span></span>

<span data-ttu-id="4505d-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="4505d-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4505d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4505d-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4505d-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="4505d-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="4505d-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4505d-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4505d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4505d-116">Requirements</span></span>



| <span data-ttu-id="4505d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4505d-117">Requirement</span></span> | <span data-ttu-id="4505d-118">Value</span><span class="sxs-lookup"><span data-stu-id="4505d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4505d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4505d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4505d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4505d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4505d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4505d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4505d-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4505d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4505d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4505d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4505d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4505d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





