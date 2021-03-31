---
title: Mensaje de PGM_GETBUTTONSTATE (commctrl. h)
description: Recupera el estado del botón especificado en un control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro GetButtonState de buscapersonas \_ .
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- PGM_GETBUTTONSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8c9eebbc0aa91651a01de1fe193544f0c8afcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996731"
---
# <a name="pgm_getbuttonstate-message"></a><span data-ttu-id="1313d-105">\_Mensaje GETBUTTONSTATE PGM</span><span class="sxs-lookup"><span data-stu-id="1313d-105">PGM\_GETBUTTONSTATE message</span></span>

<span data-ttu-id="1313d-106">Recupera el estado del botón especificado en un control de paginación.</span><span class="sxs-lookup"><span data-stu-id="1313d-106">Retrieves the state of the specified button in a pager control.</span></span> <span data-ttu-id="1313d-107">Puede enviar este mensaje explícitamente o utilizar la macro [**\_ GetButtonState de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) .</span><span class="sxs-lookup"><span data-stu-id="1313d-107">You can send this message explicitly or use the [**Pager\_GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1313d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1313d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1313d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1313d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1313d-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1313d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1313d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1313d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1313d-112">Indica el botón para el que se va a recuperar el estado.</span><span class="sxs-lookup"><span data-stu-id="1313d-112">Indicates which button to retrieve the state for.</span></span> <span data-ttu-id="1313d-113">Puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="1313d-113">This can be one of the following values:</span></span>



| <span data-ttu-id="1313d-114">Value</span><span class="sxs-lookup"><span data-stu-id="1313d-114">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="1313d-115">Significado</span><span class="sxs-lookup"><span data-stu-id="1313d-115">Meaning</span></span>                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <span data-ttu-id="1313d-116"><dt>**PGB \_ TOPORLEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="1313d-116"><dt>**PGB\_TOPORLEFT**</dt></span></span> </dl>             | <span data-ttu-id="1313d-117">Indica el botón superior de un control de paginación de [**págs \_ Vert**](pager-control-styles.md) o el botón izquierdo de un control de paginación de [**págs \_ horizontal**](pager-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1313d-117">Indicates the top button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the left button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <span data-ttu-id="1313d-118"><dt>**PGB \_ BOTTOMORRIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="1313d-118"><dt>**PGB\_BOTTOMORRIGHT**</dt></span></span> </dl> | <span data-ttu-id="1313d-119">Indica el botón inferior de un control de paginación de [**págs \_ Vert**](pager-control-styles.md) o el botón secundario en un control de paginación de [**págs \_ horizontal**](pager-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1313d-119">Indicates the bottom button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the right button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1313d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1313d-120">Return value</span></span>

<span data-ttu-id="1313d-121">Devuelve el estado del botón especificado en *lParam*.</span><span class="sxs-lookup"><span data-stu-id="1313d-121">Returns the state of the button specified in *lParam*.</span></span> <span data-ttu-id="1313d-122">Este será uno o varios de los valores siguientes (si más se devuelve un valor, se combinarán mediante una operación OR bit a bit):</span><span class="sxs-lookup"><span data-stu-id="1313d-122">This will be one or more of the following values (if more then one value is returned they will be combined using a bitwise OR):</span></span>



| <span data-ttu-id="1313d-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1313d-123">Return code</span></span>                                                                                   | <span data-ttu-id="1313d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="1313d-124">Description</span></span>                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="1313d-125"><dt>**PGF \_ invisible**</dt></span><span class="sxs-lookup"><span data-stu-id="1313d-125"><dt>**PGF\_INVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="1313d-126">El botón no está visible.</span><span class="sxs-lookup"><span data-stu-id="1313d-126">The button is not visible.</span></span> <br/>      |
| <dl> <span data-ttu-id="1313d-127"><dt>**PGF \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="1313d-127"><dt>**PGF\_NORMAL**</dt></span></span> </dl>    | <span data-ttu-id="1313d-128">El botón está en estado normal.</span><span class="sxs-lookup"><span data-stu-id="1313d-128">The button is in normal state.</span></span> <br/>  |
| <dl> <span data-ttu-id="1313d-129"><dt>**PGF \_ atenuado**</dt></span><span class="sxs-lookup"><span data-stu-id="1313d-129"><dt>**PGF\_GRAYED**</dt></span></span> </dl>    | <span data-ttu-id="1313d-130">El botón está en estado atenuado.</span><span class="sxs-lookup"><span data-stu-id="1313d-130">The button is in grayed state.</span></span> <br/>  |
| <dl> <span data-ttu-id="1313d-131"><dt>**PGF \_ presionado**</dt></span><span class="sxs-lookup"><span data-stu-id="1313d-131"><dt>**PGF\_DEPRESSED**</dt></span></span> </dl> | <span data-ttu-id="1313d-132">El botón está en estado presionado.</span><span class="sxs-lookup"><span data-stu-id="1313d-132">The button is in pressed state.</span></span> <br/> |
| <dl> <span data-ttu-id="1313d-133"><dt>**PGF en \_ caliente**</dt></span><span class="sxs-lookup"><span data-stu-id="1313d-133"><dt>**PGF\_HOT**</dt></span></span> </dl>       | <span data-ttu-id="1313d-134">El botón está en estado activo.</span><span class="sxs-lookup"><span data-stu-id="1313d-134">The button is in hot state.</span></span> <br/>     |



 

## <a name="requirements"></a><span data-ttu-id="1313d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1313d-135">Requirements</span></span>



| <span data-ttu-id="1313d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="1313d-136">Requirement</span></span> | <span data-ttu-id="1313d-137">Value</span><span class="sxs-lookup"><span data-stu-id="1313d-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1313d-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1313d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1313d-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1313d-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1313d-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1313d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1313d-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1313d-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1313d-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1313d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="1313d-143"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1313d-143"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





