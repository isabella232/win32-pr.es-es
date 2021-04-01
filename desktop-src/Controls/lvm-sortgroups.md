---
title: Mensaje de LVM_SORTGROUPS (commctrl. h)
description: Usa una función de comparación definida por la aplicación para ordenar grupos por identificador dentro de un control de vista de lista.
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- LVM_SORTGROUPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c70fd0f343c9efe0215c87f430e5ed1c89a3aed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150879"
---
# <a name="lvm_sortgroups-message"></a><span data-ttu-id="4cb4f-104">\_Mensaje SORTGROUPS LVM</span><span class="sxs-lookup"><span data-stu-id="4cb4f-104">LVM\_SORTGROUPS message</span></span>

<span data-ttu-id="4cb4f-105">Usa una función de comparación definida por la aplicación para ordenar grupos por identificador dentro de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="4cb4f-105">Uses an application-defined comparison function to sort groups by ID within a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cb4f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cb4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cb4f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cb4f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4cb4f-108">Puntero a una función de comparación definida por la aplicación, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</span><span class="sxs-lookup"><span data-stu-id="4cb4f-108">Pointer to an application-defined comparison function, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</span></span></dd> <dt>

<span data-ttu-id="4cb4f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cb4f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4cb4f-110">Puntero void a la información definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4cb4f-110">Void pointer to the application-defined information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cb4f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cb4f-111">Return value</span></span>

<span data-ttu-id="4cb4f-112">Devuelve 1 si se realiza correctamente o 0 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4cb4f-112">Returns 1 if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cb4f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4cb4f-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4cb4f-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="4cb4f-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="4cb4f-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4cb4f-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4cb4f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cb4f-116">Requirements</span></span>



| <span data-ttu-id="4cb4f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cb4f-117">Requirement</span></span> | <span data-ttu-id="4cb4f-118">Value</span><span class="sxs-lookup"><span data-stu-id="4cb4f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb4f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cb4f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4cb4f-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4cb4f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4cb4f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cb4f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4cb4f-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4cb4f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4cb4f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cb4f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cb4f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cb4f-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cb4f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cb4f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb4f-126">**LVGroupCompare**</span><span class="sxs-lookup"><span data-stu-id="4cb4f-126">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

