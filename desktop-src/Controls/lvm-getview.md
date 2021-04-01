---
title: Mensaje de LVM_GETVIEW (commctrl. h)
description: Recupera la vista actual de un control de vista de lista.
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- LVM_GETVIEW controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2da295fa5a5b335de60169ce06b777d9e355121
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150887"
---
# <a name="lvm_getview-message"></a><span data-ttu-id="2f05c-104">\_Mensaje GETVIEW (LVM</span><span class="sxs-lookup"><span data-stu-id="2f05c-104">LVM\_GETVIEW message</span></span>

<span data-ttu-id="2f05c-105">Recupera la vista actual de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="2f05c-105">Retrieves the current view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f05c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f05c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f05c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f05c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f05c-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2f05c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f05c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f05c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f05c-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2f05c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f05c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f05c-111">Return value</span></span>

<span data-ttu-id="2f05c-112">Devuelve un **valor DWORD** que especifica la vista actual.</span><span class="sxs-lookup"><span data-stu-id="2f05c-112">Returns a **DWORD** that specifies the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f05c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f05c-113">Remarks</span></span>

<span data-ttu-id="2f05c-114">A continuación se muestran los valores de las vistas.</span><span class="sxs-lookup"><span data-stu-id="2f05c-114">Following are the values for views.</span></span>

-   <span data-ttu-id="2f05c-115">detalles de la \_ vista LV \_</span><span class="sxs-lookup"><span data-stu-id="2f05c-115">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="2f05c-116">\_icono de vista de LV \_</span><span class="sxs-lookup"><span data-stu-id="2f05c-116">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="2f05c-117">\_lista de vistas de LV \_</span><span class="sxs-lookup"><span data-stu-id="2f05c-117">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="2f05c-118">visualización de la vista de LV \_ \_</span><span class="sxs-lookup"><span data-stu-id="2f05c-118">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="2f05c-119">\_icono de vista de LV \_</span><span class="sxs-lookup"><span data-stu-id="2f05c-119">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="2f05c-120">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="2f05c-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2f05c-121">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2f05c-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2f05c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f05c-122">Requirements</span></span>



| <span data-ttu-id="2f05c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f05c-123">Requirement</span></span> | <span data-ttu-id="2f05c-124">Value</span><span class="sxs-lookup"><span data-stu-id="2f05c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f05c-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f05c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2f05c-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2f05c-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f05c-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f05c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2f05c-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f05c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f05c-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f05c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f05c-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f05c-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





