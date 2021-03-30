---
title: Mensaje de HDM_CREATEDRAGIMAGE (commctrl. h)
description: Crea una versión semitransparente de la imagen de un elemento para su uso como una imagen de arrastre. Puede enviar este mensaje explícitamente o utilizar la \_ macro header CreateDragImage.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- HDM_CREATEDRAGIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e801ad9771205b5f2e6df8e37bb0a0ad7f0bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079530"
---
# <a name="hdm_createdragimage-message"></a><span data-ttu-id="4cf2f-105">HDM \_ CREATEDRAGIMAGE</span><span class="sxs-lookup"><span data-stu-id="4cf2f-105">HDM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="4cf2f-106">Crea una versión semitransparente de la imagen de un elemento para su uso como una imagen de arrastre.</span><span class="sxs-lookup"><span data-stu-id="4cf2f-106">Creates a semi-transparent version of an item's image for use as a dragging image.</span></span> <span data-ttu-id="4cf2f-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="4cf2f-107">You can send this message explicitly or use the [**Header\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cf2f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cf2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cf2f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cf2f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cf2f-110">Índice de base cero del elemento dentro del control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="4cf2f-110">The zero-based index of the item within the header control.</span></span> <span data-ttu-id="4cf2f-111">La imagen asignada a este elemento es la base de la imagen transparente.</span><span class="sxs-lookup"><span data-stu-id="4cf2f-111">The image assigned to this item is the basis for the transparent image.</span></span>

</dd> <dt>

<span data-ttu-id="4cf2f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cf2f-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4cf2f-113">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4cf2f-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cf2f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cf2f-114">Return value</span></span>

<span data-ttu-id="4cf2f-115">Devuelve un identificador a una lista de imágenes que contiene la nueva imagen como su único elemento.</span><span class="sxs-lookup"><span data-stu-id="4cf2f-115">Returns a handle to an image list that contains the new image as its only element.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cf2f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cf2f-116">Requirements</span></span>



| <span data-ttu-id="4cf2f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cf2f-117">Requirement</span></span> | <span data-ttu-id="4cf2f-118">Value</span><span class="sxs-lookup"><span data-stu-id="4cf2f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf2f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cf2f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf2f-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4cf2f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4cf2f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cf2f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf2f-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4cf2f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4cf2f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cf2f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cf2f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cf2f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





