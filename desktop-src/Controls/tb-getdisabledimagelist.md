---
title: Mensaje de TB_GETDISABLEDIMAGELIST (commctrl. h)
description: Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar botones inactivos.
ms.assetid: 8f6782d5-488b-4906-908a-e4bf8d512e0a
keywords:
- TB_GETDISABLEDIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc847927ef14312c76e26303bec5de07b788266
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996284"
---
# <a name="tb_getdisabledimagelist-message"></a><span data-ttu-id="ff381-104">\_Mensaje GETDISABLEDIMAGELIST TB</span><span class="sxs-lookup"><span data-stu-id="ff381-104">TB\_GETDISABLEDIMAGELIST message</span></span>

<span data-ttu-id="ff381-105">Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar botones inactivos.</span><span class="sxs-lookup"><span data-stu-id="ff381-105">Retrieves the image list that a toolbar control uses to display inactive buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff381-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff381-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff381-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff381-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ff381-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ff381-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ff381-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff381-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ff381-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ff381-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff381-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff381-111">Return value</span></span>

<span data-ttu-id="ff381-112">Devuelve el identificador de la lista de imágenes inactivas, o **null** si no se establece ninguna lista de imágenes inactiva.</span><span class="sxs-lookup"><span data-stu-id="ff381-112">Returns the handle to the inactive image list, or **NULL** if no inactive image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff381-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff381-113">Requirements</span></span>



| <span data-ttu-id="ff381-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff381-114">Requirement</span></span> | <span data-ttu-id="ff381-115">Value</span><span class="sxs-lookup"><span data-stu-id="ff381-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff381-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff381-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ff381-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ff381-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff381-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff381-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ff381-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff381-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff381-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff381-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff381-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff381-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





