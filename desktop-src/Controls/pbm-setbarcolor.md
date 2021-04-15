---
title: Mensaje de PBM_SETBARCOLOR (commctrl. h)
description: Establece el color de la barra de indicador de progreso en el control de barra de progreso.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- PBM_SETBARCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1387e69622e84990a197dc5a374d1c3449393408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534672"
---
# <a name="pbm_setbarcolor-message"></a><span data-ttu-id="8f390-104">Mensaje de SETBARCOLOR de PBM \_</span><span class="sxs-lookup"><span data-stu-id="8f390-104">PBM\_SETBARCOLOR message</span></span>

<span data-ttu-id="8f390-105">Establece el color de la barra de indicador de progreso en el control de barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="8f390-105">Sets the color of the progress indicator bar in the progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f390-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f390-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f390-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f390-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f390-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8f390-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8f390-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f390-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f390-110">Valor **COLORREF** que especifica el nuevo color de la barra del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="8f390-110">The **COLORREF** value that specifies the new progress indicator bar color.</span></span> <span data-ttu-id="8f390-111">Si se especifica el \_ valor predeterminado de CLR, la barra de progreso usará el color predeterminado de la barra del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="8f390-111">Specifying the CLR\_DEFAULT value causes the progress bar to use its default progress indicator bar color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f390-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f390-112">Return value</span></span>

<span data-ttu-id="8f390-113">Devuelve el color de la barra del indicador de progreso anterior, o el \_ valor predeterminado de CLR si el color de la barra indicadora de progreso es el color predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8f390-113">Returns the previous progress indicator bar color, or CLR\_DEFAULT if the progress indicator bar color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f390-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f390-114">Remarks</span></span>

<span data-ttu-id="8f390-115">Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="8f390-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f390-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f390-116">Requirements</span></span>



| <span data-ttu-id="8f390-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f390-117">Requirement</span></span> | <span data-ttu-id="8f390-118">Value</span><span class="sxs-lookup"><span data-stu-id="8f390-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f390-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f390-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8f390-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8f390-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f390-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f390-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8f390-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f390-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f390-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f390-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f390-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f390-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





