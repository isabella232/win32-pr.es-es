---
title: Mensaje de TVM_CREATEDRAGIMAGE (commctrl. h)
description: Crea un mapa de bits de arrastre para el elemento especificado en un control de vista de árbol.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- TVM_CREATEDRAGIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189b37affc6a4382541faea13199cacfcb9b7df5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150360"
---
# <a name="tvm_createdragimage-message"></a><span data-ttu-id="4cdaa-104">\_Mensaje de CREATEDRAGIMAGE TVM</span><span class="sxs-lookup"><span data-stu-id="4cdaa-104">TVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="4cdaa-105">Crea un mapa de bits de arrastre para el elemento especificado en un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="4cdaa-105">Creates a dragging bitmap for the specified item in a tree-view control.</span></span> <span data-ttu-id="4cdaa-106">El mensaje también crea una lista de imágenes para el mapa de bits y agrega el mapa de bits a la lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="4cdaa-106">The message also creates an image list for the bitmap and adds the bitmap to the image list.</span></span> <span data-ttu-id="4cdaa-107">Una aplicación puede mostrar la imagen al arrastrar el elemento mediante las funciones de la lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="4cdaa-107">An application can display the image when dragging the item by using the image list functions.</span></span> <span data-ttu-id="4cdaa-108">Puede enviar este mensaje explícitamente o mediante la macro [**\_ CreateDragImage de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="4cdaa-108">You can send this message explicitly or by using the [**TreeView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cdaa-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cdaa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cdaa-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cdaa-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4cdaa-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4cdaa-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4cdaa-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cdaa-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cdaa-113">Identificador del elemento que recibe el nuevo mapa de bits de arrastre.</span><span class="sxs-lookup"><span data-stu-id="4cdaa-113">Handle to the item that receives the new dragging bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cdaa-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cdaa-114">Return value</span></span>

<span data-ttu-id="4cdaa-115">Devuelve el identificador de la lista de imágenes a la que se agregó el mapa de bits de arrastre si se realiza correctamente, o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4cdaa-115">Returns the handle to the image list to which the dragging bitmap was added if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cdaa-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4cdaa-116">Remarks</span></span>

<span data-ttu-id="4cdaa-117">Si crea un control de vista de árbol sin una lista de imágenes asociada, no puede usar el mensaje **TVM \_ CREATEDRAGIMAGE** para crear la imagen que se va a mostrar durante una operación de arrastre.</span><span class="sxs-lookup"><span data-stu-id="4cdaa-117">If you create a tree-view control without an associated image list, you cannot use the **TVM\_CREATEDRAGIMAGE** message to create the image to display during a drag operation.</span></span> <span data-ttu-id="4cdaa-118">Debe implementar su propio método para crear un cursor de arrastre.</span><span class="sxs-lookup"><span data-stu-id="4cdaa-118">You must implement your own method of creating a drag cursor.</span></span>

<span data-ttu-id="4cdaa-119">La aplicación es responsable de destruir la lista de imágenes cuando ya no se necesita.</span><span class="sxs-lookup"><span data-stu-id="4cdaa-119">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cdaa-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cdaa-120">Requirements</span></span>



| <span data-ttu-id="4cdaa-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cdaa-121">Requirement</span></span> | <span data-ttu-id="4cdaa-122">Value</span><span class="sxs-lookup"><span data-stu-id="4cdaa-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdaa-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cdaa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4cdaa-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4cdaa-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4cdaa-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cdaa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4cdaa-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4cdaa-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4cdaa-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cdaa-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cdaa-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cdaa-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





