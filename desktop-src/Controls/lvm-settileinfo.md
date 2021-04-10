---
title: Mensaje de LVM_SETTILEINFO (commctrl. h)
description: Establece la información de un icono existente de un control de vista de lista.
ms.assetid: 345e8f16-9a6c-44e3-a262-d5d3be4d33ef
keywords:
- LVM_SETTILEINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489e163955b8f9cbf99ad25357b5be5a5d5981fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150130"
---
# <a name="lvm_settileinfo-message"></a><span data-ttu-id="bdc88-104">\_Mensaje SETTILEINFO LVM</span><span class="sxs-lookup"><span data-stu-id="bdc88-104">LVM\_SETTILEINFO message</span></span>

<span data-ttu-id="bdc88-105">Establece la información de un icono existente de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="bdc88-105">Sets information for an existing tile of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdc88-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bdc88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdc88-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdc88-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bdc88-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bdc88-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bdc88-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdc88-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bdc88-110">Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> que contiene la información que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="bdc88-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdc88-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bdc88-111">Return value</span></span>

<span data-ttu-id="bdc88-112">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bdc88-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdc88-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdc88-113">Remarks</span></span>

<span data-ttu-id="bdc88-114">**LVM \_ SETTILEINFO** no se admite en el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="bdc88-114">**LVM\_SETTILEINFO** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="bdc88-115">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="bdc88-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="bdc88-116">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bdc88-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bdc88-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdc88-117">Requirements</span></span>



| <span data-ttu-id="bdc88-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdc88-118">Requirement</span></span> | <span data-ttu-id="bdc88-119">Value</span><span class="sxs-lookup"><span data-stu-id="bdc88-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc88-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdc88-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc88-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bdc88-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bdc88-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdc88-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc88-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bdc88-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdc88-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bdc88-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdc88-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdc88-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





