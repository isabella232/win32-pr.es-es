---
title: Mensaje de LVM_SETTILEVIEWINFO (commctrl. h)
description: Establece la información que usa un control de vista de lista en la vista de mosaico.
ms.assetid: 1c4f2aff-1ce1-484a-9360-3efbe870b39b
keywords:
- LVM_SETTILEVIEWINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25d6c728d92bb931837eca440af679b5bcb98d1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150129"
---
# <a name="lvm_settileviewinfo-message"></a><span data-ttu-id="9ab1d-104">\_Mensaje SETTILEVIEWINFO LVM</span><span class="sxs-lookup"><span data-stu-id="9ab1d-104">LVM\_SETTILEVIEWINFO message</span></span>

<span data-ttu-id="9ab1d-105">Establece la información que usa un control de vista de lista en la vista de mosaico.</span><span class="sxs-lookup"><span data-stu-id="9ab1d-105">Sets information that a list-view control uses in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ab1d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ab1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ab1d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ab1d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9ab1d-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9ab1d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9ab1d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ab1d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9ab1d-110">Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> que contiene la información que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="9ab1d-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ab1d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ab1d-111">Return value</span></span>

<span data-ttu-id="9ab1d-112">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9ab1d-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ab1d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ab1d-113">Remarks</span></span>

<span data-ttu-id="9ab1d-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="9ab1d-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="9ab1d-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9ab1d-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ab1d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ab1d-116">Requirements</span></span>



| <span data-ttu-id="9ab1d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ab1d-117">Requirement</span></span> | <span data-ttu-id="9ab1d-118">Value</span><span class="sxs-lookup"><span data-stu-id="9ab1d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab1d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ab1d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9ab1d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9ab1d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ab1d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ab1d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9ab1d-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ab1d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ab1d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ab1d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ab1d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ab1d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





