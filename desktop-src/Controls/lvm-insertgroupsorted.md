---
title: Mensaje de LVM_INSERTGROUPSORTED (commctrl. h)
description: Inserta un grupo en una lista ordenada de grupos.
ms.assetid: 8ad1660b-8b64-4f02-ac1b-b7edeeea38ab
keywords:
- LVM_INSERTGROUPSORTED controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_INSERTGROUPSORTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 485941f803fd5af565d8b40524a9e15968e387cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905499"
---
# <a name="lvm_insertgroupsorted-message"></a><span data-ttu-id="9c7c2-104">\_Mensaje INSERTGROUPSORTED LVM</span><span class="sxs-lookup"><span data-stu-id="9c7c2-104">LVM\_INSERTGROUPSORTED message</span></span>

<span data-ttu-id="9c7c2-105">Inserta un grupo en una lista ordenada de grupos.</span><span class="sxs-lookup"><span data-stu-id="9c7c2-105">Inserts a group into an ordered list of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c7c2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c7c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c7c2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c7c2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9c7c2-108">Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a> que contiene el grupo que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="9c7c2-108">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a> structure that contains the group to insert.</span></span></dd> <dt>

<span data-ttu-id="9c7c2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c7c2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9c7c2-110">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="9c7c2-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c7c2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c7c2-111">Return value</span></span>

<span data-ttu-id="9c7c2-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="9c7c2-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c7c2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c7c2-113">Remarks</span></span>

<span data-ttu-id="9c7c2-114">El orden de la lista se basa en el identificador del grupo.</span><span class="sxs-lookup"><span data-stu-id="9c7c2-114">The ordering of the list is based on the ID of the group.</span></span> <span data-ttu-id="9c7c2-115">El orden se define mediante la función de ordenación definida por la aplicación, [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), que se pasa en la estructura [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) mediante el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="9c7c2-115">The order is defined by the application-defined ordering function, [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), that is passed in the [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) structure by the *wParam* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="9c7c2-116">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="9c7c2-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="9c7c2-117">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9c7c2-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9c7c2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c7c2-118">Requirements</span></span>



| <span data-ttu-id="9c7c2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c7c2-119">Requirement</span></span> | <span data-ttu-id="9c7c2-120">Value</span><span class="sxs-lookup"><span data-stu-id="9c7c2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c7c2-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c7c2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9c7c2-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9c7c2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c7c2-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c7c2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9c7c2-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c7c2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c7c2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c7c2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c7c2-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c7c2-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c7c2-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c7c2-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c7c2-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9c7c2-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c7c2-129">**LVGroupCompare**</span><span class="sxs-lookup"><span data-stu-id="9c7c2-129">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> <dt>

[<span data-ttu-id="9c7c2-130">**LVINSERTGROUPSORTED**</span><span class="sxs-lookup"><span data-stu-id="9c7c2-130">**LVINSERTGROUPSORTED**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
</dt> </dl>

 

