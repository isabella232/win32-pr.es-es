---
title: Mensaje de PGM_SETPOS (commctrl. h)
description: Establece la posición de desplazamiento actual para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro setPos de buscapersonas \_ .
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- PGM_SETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802066"
---
# <a name="pgm_setpos-message"></a><span data-ttu-id="04a76-105">\_Mensaje SETPOS PGM</span><span class="sxs-lookup"><span data-stu-id="04a76-105">PGM\_SETPOS message</span></span>

<span data-ttu-id="04a76-106">Establece la posición de desplazamiento actual para el control de paginación.</span><span class="sxs-lookup"><span data-stu-id="04a76-106">Sets the current scroll position for the pager control.</span></span> <span data-ttu-id="04a76-107">Puede enviar este mensaje explícitamente o utilizar la macro [**\_ setPos de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) .</span><span class="sxs-lookup"><span data-stu-id="04a76-107">You can send this message explicitly or use the [**Pager\_SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="04a76-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04a76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04a76-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04a76-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="04a76-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="04a76-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="04a76-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04a76-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04a76-112">Valor de tipo **int** que contiene la nueva posición de desplazamiento, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="04a76-112">Value of type **int** that contains the new scroll position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04a76-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04a76-113">Return value</span></span>

<span data-ttu-id="04a76-114">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="04a76-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="04a76-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04a76-115">Requirements</span></span>



| <span data-ttu-id="04a76-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="04a76-116">Requirement</span></span> | <span data-ttu-id="04a76-117">Value</span><span class="sxs-lookup"><span data-stu-id="04a76-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04a76-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04a76-118">Minimum supported client</span></span><br/> | <span data-ttu-id="04a76-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="04a76-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04a76-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04a76-120">Minimum supported server</span></span><br/> | <span data-ttu-id="04a76-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="04a76-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04a76-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04a76-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="04a76-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="04a76-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





