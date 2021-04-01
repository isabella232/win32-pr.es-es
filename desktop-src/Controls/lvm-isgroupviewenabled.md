---
title: Mensaje de LVM_ISGROUPVIEWENABLED (commctrl. h)
description: Comprueba si el control de vista de lista tiene la vista de grupo habilitada.
ms.assetid: 7c6ffa1f-300c-4e5e-900f-93a41e06c951
keywords:
- LVM_ISGROUPVIEWENABLED controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_ISGROUPVIEWENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8f7af79a1b0594ba6ebb100c1c975f09898d35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996904"
---
# <a name="lvm_isgroupviewenabled-message"></a><span data-ttu-id="afaf0-104">\_Mensaje ISGROUPVIEWENABLED LVM</span><span class="sxs-lookup"><span data-stu-id="afaf0-104">LVM\_ISGROUPVIEWENABLED message</span></span>

<span data-ttu-id="afaf0-105">Comprueba si el control de vista de lista tiene la vista de grupo habilitada.</span><span class="sxs-lookup"><span data-stu-id="afaf0-105">Checks whether the list-view control has group view enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="afaf0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afaf0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afaf0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="afaf0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="afaf0-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="afaf0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="afaf0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afaf0-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="afaf0-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="afaf0-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afaf0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afaf0-111">Return value</span></span>

<span data-ttu-id="afaf0-112">Devuelve **true** si la vista de grupo está habilitada o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="afaf0-112">Returns **TRUE** if group view is enabled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="afaf0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="afaf0-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="afaf0-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="afaf0-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="afaf0-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="afaf0-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="afaf0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afaf0-116">Requirements</span></span>



| <span data-ttu-id="afaf0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="afaf0-117">Requirement</span></span> | <span data-ttu-id="afaf0-118">Value</span><span class="sxs-lookup"><span data-stu-id="afaf0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afaf0-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afaf0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="afaf0-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="afaf0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="afaf0-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afaf0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="afaf0-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="afaf0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afaf0-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afaf0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="afaf0-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="afaf0-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





