---
title: Mensaje de TB_GETIMAGELIST (commctrl. h)
description: Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar los botones en su estado predeterminado. Un control de barra de herramientas usa esta lista de imágenes para mostrar botones cuando no están activos o deshabilitados.
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- TB_GETIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a56b8b847bd212e703d3b512b255cf1693abf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801357"
---
# <a name="tb_getimagelist-message"></a><span data-ttu-id="50cd0-105">\_Mensaje GETIMAGELIST TB</span><span class="sxs-lookup"><span data-stu-id="50cd0-105">TB\_GETIMAGELIST message</span></span>

<span data-ttu-id="50cd0-106">Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar los botones en su estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="50cd0-106">Retrieves the image list that a toolbar control uses to display buttons in their default state.</span></span> <span data-ttu-id="50cd0-107">Un control de barra de herramientas usa esta lista de imágenes para mostrar botones cuando no están activos o deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="50cd0-107">A toolbar control uses this image list to display buttons when they are not hot or disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="50cd0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50cd0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50cd0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50cd0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50cd0-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="50cd0-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="50cd0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50cd0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50cd0-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="50cd0-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50cd0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50cd0-113">Return value</span></span>

<span data-ttu-id="50cd0-114">Devuelve el identificador de la lista de imágenes o **null** si no se ha establecido ninguna lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="50cd0-114">Returns the handle to the image list, or **NULL** if no image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="50cd0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50cd0-115">Requirements</span></span>



| <span data-ttu-id="50cd0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="50cd0-116">Requirement</span></span> | <span data-ttu-id="50cd0-117">Value</span><span class="sxs-lookup"><span data-stu-id="50cd0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50cd0-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50cd0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="50cd0-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="50cd0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50cd0-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50cd0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="50cd0-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="50cd0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50cd0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50cd0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="50cd0-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="50cd0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





