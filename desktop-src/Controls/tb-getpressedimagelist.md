---
title: Mensaje de TB_GETPRESSEDIMAGELIST (commctrl. h)
description: Obtiene la lista de imágenes que usa un control de barra de herramientas para mostrar los botones en estado presionado.
ms.assetid: 116d4212-48ea-4b00-a752-21e5e1f10e36
keywords:
- TB_GETPRESSEDIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETPRESSEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3028b119eb7f84a66caf0b6978382cee569b4a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151206"
---
# <a name="tb_getpressedimagelist-message"></a><span data-ttu-id="af8a6-104">\_Mensaje GETPRESSEDIMAGELIST TB</span><span class="sxs-lookup"><span data-stu-id="af8a6-104">TB\_GETPRESSEDIMAGELIST message</span></span>

<span data-ttu-id="af8a6-105">Obtiene la lista de imágenes que usa un control de barra de herramientas para mostrar los botones en estado presionado.</span><span class="sxs-lookup"><span data-stu-id="af8a6-105">Gets the image list that a toolbar control uses to display buttons in a pressed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="af8a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af8a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af8a6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af8a6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af8a6-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="af8a6-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="af8a6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af8a6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af8a6-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="af8a6-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af8a6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af8a6-111">Return value</span></span>

<span data-ttu-id="af8a6-112">Devuelve el identificador de la lista de imágenes o **null** si no se ha establecido ninguna lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="af8a6-112">Returns the handle to the image list, or **NULL** if no image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="af8a6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af8a6-113">Requirements</span></span>



| <span data-ttu-id="af8a6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="af8a6-114">Requirement</span></span> | <span data-ttu-id="af8a6-115">Value</span><span class="sxs-lookup"><span data-stu-id="af8a6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af8a6-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af8a6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="af8a6-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="af8a6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af8a6-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af8a6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="af8a6-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="af8a6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af8a6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af8a6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="af8a6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="af8a6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





