---
title: Mensaje de LVM_ENABLEGROUPVIEW (commctrl. h)
description: Habilita o deshabilita si los elementos de un control de vista de lista se muestran como un grupo.
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- LVM_ENABLEGROUPVIEW controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_ENABLEGROUPVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d546e1236fa4f0800c0353810beb5b427ba4fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078876"
---
# <a name="lvm_enablegroupview-message"></a><span data-ttu-id="6c73c-104">\_Mensaje ENABLEGROUPVIEW LVM</span><span class="sxs-lookup"><span data-stu-id="6c73c-104">LVM\_ENABLEGROUPVIEW message</span></span>

<span data-ttu-id="6c73c-105">Habilita o deshabilita si los elementos de un control de vista de lista se muestran como un grupo.</span><span class="sxs-lookup"><span data-stu-id="6c73c-105">Enables or disables whether the items in a list-view control display as a group.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c73c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c73c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c73c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c73c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6c73c-108">Un **booleano** que indica si se va a habilitar un control de vista de lista para agrupar los elementos mostrados.</span><span class="sxs-lookup"><span data-stu-id="6c73c-108">A **BOOL** that indicates whether to enable a list-view control to group displayed items.</span></span> <span data-ttu-id="6c73c-109">Use **true** para habilitar la agrupación y **false** para deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="6c73c-109">Use **TRUE** to enable grouping, **FALSE** to disable it.</span></span> </dd> <dt>

<span data-ttu-id="6c73c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c73c-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6c73c-111">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="6c73c-111">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c73c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c73c-112">Return value</span></span>

<span data-ttu-id="6c73c-113">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6c73c-113">Returns one of the following values.</span></span>



| <span data-ttu-id="6c73c-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6c73c-114">Return code</span></span>                                                                       | <span data-ttu-id="6c73c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c73c-115">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c73c-116"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="6c73c-116"><dt>**0**</dt></span></span> </dl>  | <span data-ttu-id="6c73c-117">La capacidad de mostrar los elementos de vista de lista como un grupo ya está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="6c73c-117">The ability to display list-view items as a group is already enabled or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="6c73c-118"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="6c73c-118"><dt>**1**</dt></span></span> </dl>  | <span data-ttu-id="6c73c-119">El estado del control se ha cambiado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6c73c-119">The state of the control was successfully changed.</span></span><br/>                                |
| <dl> <span data-ttu-id="6c73c-120"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="6c73c-120"><dt>**-1**</dt></span></span> </dl> | <span data-ttu-id="6c73c-121">Error en la operación.</span><span class="sxs-lookup"><span data-stu-id="6c73c-121">The operation failed.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="6c73c-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c73c-122">Remarks</span></span>

<span data-ttu-id="6c73c-123">**LVM \_ ENABLEGROUPVIEW** no se admite en el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6c73c-123">**LVM\_ENABLEGROUPVIEW** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="6c73c-124">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="6c73c-124">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6c73c-125">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6c73c-125">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6c73c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c73c-126">Requirements</span></span>



| <span data-ttu-id="6c73c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c73c-127">Requirement</span></span> | <span data-ttu-id="6c73c-128">Value</span><span class="sxs-lookup"><span data-stu-id="6c73c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c73c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c73c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6c73c-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6c73c-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c73c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c73c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6c73c-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c73c-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c73c-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c73c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c73c-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c73c-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





