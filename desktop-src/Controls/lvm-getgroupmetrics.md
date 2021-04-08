---
title: Mensaje de LVM_GETGROUPMETRICS (commctrl. h)
description: Obtiene información acerca de la presentación de grupos.
ms.assetid: 75e7da66-50c6-4834-ae66-e43b8f9b0b34
keywords:
- LVM_GETGROUPMETRICS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5af8ec50fe74ab90a0f3e44a69e2cbc7dda583e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996918"
---
# <a name="lvm_getgroupmetrics-message"></a><span data-ttu-id="0a33c-104">\_Mensaje GETGROUPMETRICS LVM</span><span class="sxs-lookup"><span data-stu-id="0a33c-104">LVM\_GETGROUPMETRICS message</span></span>

<span data-ttu-id="0a33c-105">Obtiene información acerca de la presentación de grupos.</span><span class="sxs-lookup"><span data-stu-id="0a33c-105">Gets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a33c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a33c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a33c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a33c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0a33c-108">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="0a33c-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="0a33c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a33c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0a33c-110">Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> que recibe las métricas recuperadas.</span><span class="sxs-lookup"><span data-stu-id="0a33c-110">A pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that receives the retrieved metrics.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a33c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a33c-111">Return value</span></span>

<span data-ttu-id="0a33c-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="0a33c-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a33c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a33c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0a33c-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="0a33c-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="0a33c-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0a33c-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a33c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a33c-116">Requirements</span></span>



| <span data-ttu-id="0a33c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a33c-117">Requirement</span></span> | <span data-ttu-id="0a33c-118">Value</span><span class="sxs-lookup"><span data-stu-id="0a33c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a33c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a33c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0a33c-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0a33c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a33c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a33c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0a33c-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a33c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a33c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a33c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a33c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a33c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





