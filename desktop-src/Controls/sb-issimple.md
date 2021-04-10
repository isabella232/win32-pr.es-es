---
title: Mensaje de SB_ISSIMPLE (commctrl. h)
description: Comprueba un control de barra de estado para determinar si está en modo simple.
ms.assetid: f4362bc3-1852-4569-af9b-96d2da4f0606
keywords:
- SB_ISSIMPLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_ISSIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a5c523bef45065b103051962d7f147816c505d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150751"
---
# <a name="sb_issimple-message"></a><span data-ttu-id="f2062-104">\_Mensaje ISSIMPLE de SB</span><span class="sxs-lookup"><span data-stu-id="f2062-104">SB\_ISSIMPLE message</span></span>

<span data-ttu-id="f2062-105">Comprueba un control de barra de estado para determinar si está en modo simple.</span><span class="sxs-lookup"><span data-stu-id="f2062-105">Checks a status bar control to determine if it is in simple mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2062-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2062-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2062-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2062-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f2062-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f2062-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f2062-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2062-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f2062-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f2062-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2062-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2062-111">Return value</span></span>

<span data-ttu-id="f2062-112">Devuelve un valor distinto de cero si el control de barra de estado está en modo simple o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f2062-112">Returns nonzero if the status bar control is in simple mode, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2062-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2062-113">Requirements</span></span>



| <span data-ttu-id="f2062-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2062-114">Requirement</span></span> | <span data-ttu-id="f2062-115">Value</span><span class="sxs-lookup"><span data-stu-id="f2062-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2062-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2062-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f2062-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f2062-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2062-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2062-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f2062-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2062-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2062-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2062-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2062-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2062-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





