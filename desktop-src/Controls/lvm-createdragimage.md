---
title: Mensaje de LVM_CREATEDRAGIMAGE (commctrl. h)
description: Crea una lista de imágenes de arrastre para el elemento especificado. Puede enviar este mensaje explícitamente o mediante la \_ macro CreateDragImage de ListView.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- LVM_CREATEDRAGIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace975b178fee85e2794b518a78b40b375c65ae7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149906"
---
# <a name="lvm_createdragimage-message"></a><span data-ttu-id="c8149-105">\_Mensaje CREATEDRAGIMAGE LVM</span><span class="sxs-lookup"><span data-stu-id="c8149-105">LVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="c8149-106">Crea una lista de imágenes de arrastre para el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="c8149-106">Creates a drag image list for the specified item.</span></span> <span data-ttu-id="c8149-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ CreateDragImage de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="c8149-107">You can send this message explicitly or by using the [**ListView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8149-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8149-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8149-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8149-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8149-110">Índice del elemento.</span><span class="sxs-lookup"><span data-stu-id="c8149-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="c8149-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8149-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8149-112">Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que recibe la ubicación inicial de la esquina superior izquierda de la imagen, en coordenadas de la vista.</span><span class="sxs-lookup"><span data-stu-id="c8149-112">A pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the initial location of the upper-left corner of the image, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8149-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8149-113">Return value</span></span>

<span data-ttu-id="c8149-114">Devuelve el identificador de la lista de imágenes de arrastre si se realiza correctamente o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c8149-114">Returns the handle to the drag image list if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8149-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8149-115">Remarks</span></span>

<span data-ttu-id="c8149-116">La aplicación es responsable de destruir la lista de imágenes cuando ya no se necesita.</span><span class="sxs-lookup"><span data-stu-id="c8149-116">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8149-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8149-117">Requirements</span></span>



| <span data-ttu-id="c8149-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8149-118">Requirement</span></span> | <span data-ttu-id="c8149-119">Value</span><span class="sxs-lookup"><span data-stu-id="c8149-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8149-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8149-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c8149-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c8149-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8149-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8149-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c8149-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8149-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8149-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8149-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8149-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8149-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

