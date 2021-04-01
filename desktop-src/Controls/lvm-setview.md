---
title: Mensaje de LVM_SETVIEW (commctrl. h)
description: Establece la vista de un control de vista de lista.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- LVM_SETVIEW controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159710b3086bcba5298a5a88f9cab15f76e0d89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150880"
---
# <a name="lvm_setview-message"></a><span data-ttu-id="2bda8-104">\_Mensaje SETVIEW LVM</span><span class="sxs-lookup"><span data-stu-id="2bda8-104">LVM\_SETVIEW message</span></span>

<span data-ttu-id="2bda8-105">Establece la vista de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="2bda8-105">Sets the view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2bda8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bda8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bda8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2bda8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2bda8-108">**DWORD** que especifica la vista.</span><span class="sxs-lookup"><span data-stu-id="2bda8-108">**DWORD** that specifies the view.</span></span></dd> <dt>

<span data-ttu-id="2bda8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2bda8-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2bda8-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2bda8-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bda8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bda8-111">Return value</span></span>

<span data-ttu-id="2bda8-112">Devuelve 1 si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2bda8-112">Returns 1 if successful, or -1 otherwise.</span></span> <span data-ttu-id="2bda8-113">Por ejemplo, se devuelve-1 si la vista no es válida.</span><span class="sxs-lookup"><span data-stu-id="2bda8-113">For example, -1 is returned if the view is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bda8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bda8-114">Remarks</span></span>

<span data-ttu-id="2bda8-115">A continuación se muestran los valores de las vistas.</span><span class="sxs-lookup"><span data-stu-id="2bda8-115">Following are the values for views.</span></span>

-   <span data-ttu-id="2bda8-116">detalles de la \_ vista LV \_</span><span class="sxs-lookup"><span data-stu-id="2bda8-116">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="2bda8-117">\_icono de vista de LV \_</span><span class="sxs-lookup"><span data-stu-id="2bda8-117">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="2bda8-118">\_lista de vistas de LV \_</span><span class="sxs-lookup"><span data-stu-id="2bda8-118">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="2bda8-119">visualización de la vista de LV \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bda8-119">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="2bda8-120">\_icono de vista de LV \_</span><span class="sxs-lookup"><span data-stu-id="2bda8-120">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="2bda8-121">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comctl32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="2bda8-121">To use this message, you must provide a manifest specifying Comctl32.dll version 6.0.</span></span> <span data-ttu-id="2bda8-122">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2bda8-122">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2bda8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bda8-123">Requirements</span></span>



| <span data-ttu-id="2bda8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bda8-124">Requirement</span></span> | <span data-ttu-id="2bda8-125">Value</span><span class="sxs-lookup"><span data-stu-id="2bda8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bda8-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bda8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2bda8-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2bda8-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2bda8-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bda8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2bda8-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2bda8-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2bda8-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bda8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bda8-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bda8-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





