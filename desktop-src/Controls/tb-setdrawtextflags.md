---
title: Mensaje de TB_SETDRAWTEXTFLAGS (commctrl. h)
description: Establece las marcas de dibujo de texto de la barra de herramientas.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- TB_SETDRAWTEXTFLAGS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890a24239ff2257ffaccff6613b3765711b2ef7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996801"
---
# <a name="tb_setdrawtextflags-message"></a><span data-ttu-id="eaa04-104">\_Mensaje SETDRAWTEXTFLAGS TB</span><span class="sxs-lookup"><span data-stu-id="eaa04-104">TB\_SETDRAWTEXTFLAGS message</span></span>

<span data-ttu-id="eaa04-105">Establece las marcas de dibujo de texto de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="eaa04-105">Sets the text drawing flags for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="eaa04-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eaa04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaa04-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eaa04-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eaa04-108">Una o varias de las \_ marcas DT, especificadas en [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), que indican qué bits de *lParam* se utilizarán al dibujar el texto.</span><span class="sxs-lookup"><span data-stu-id="eaa04-108">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate which bits in *lParam* will be used when drawing the text.</span></span>

</dd> <dt>

<span data-ttu-id="eaa04-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eaa04-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eaa04-110">Una o varias de las \_ marcas DT, especificadas en [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), que indican cómo se dibujará el texto del botón.</span><span class="sxs-lookup"><span data-stu-id="eaa04-110">One or more of the DT\_ flags, specified in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), that indicate how the button text will be drawn.</span></span> <span data-ttu-id="eaa04-111">Este valor se pasará a la función **DrawText** cuando se dibuje el texto del botón.</span><span class="sxs-lookup"><span data-stu-id="eaa04-111">This value will be passed to the **DrawText** function when the button text is drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaa04-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eaa04-112">Return value</span></span>

<span data-ttu-id="eaa04-113">Devuelve las marcas de dibujo de texto anteriores.</span><span class="sxs-lookup"><span data-stu-id="eaa04-113">Returns the previous text drawing flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaa04-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eaa04-114">Remarks</span></span>

<span data-ttu-id="eaa04-115">El parámetro *wParam* le permite especificar qué marcas se utilizarán al dibujar el texto, aunque estas marcas estén desactivadas.</span><span class="sxs-lookup"><span data-stu-id="eaa04-115">The *wParam* parameter allows you to specify which flags will be used when drawing the text, even if these flags are turned off.</span></span> <span data-ttu-id="eaa04-116">Por ejemplo, si no desea que se use la \_ marca DT Center al dibujar texto, debe agregar la marca DT \_ Center a *wParam* y no especificar la marca DT \_ Center en *lParam*.</span><span class="sxs-lookup"><span data-stu-id="eaa04-116">For example, if you do not want the DT\_CENTER flag used when drawing text, you would add the DT\_CENTER flag to *wParam* and not specify the DT\_CENTER flag in *lParam*.</span></span> <span data-ttu-id="eaa04-117">Esto evita que el control pase la \_ marca DT Center a la función [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .</span><span class="sxs-lookup"><span data-stu-id="eaa04-117">This prevents the control from passing the DT\_CENTER flag to the [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaa04-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaa04-118">Requirements</span></span>



| <span data-ttu-id="eaa04-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaa04-119">Requirement</span></span> | <span data-ttu-id="eaa04-120">Value</span><span class="sxs-lookup"><span data-stu-id="eaa04-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa04-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eaa04-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eaa04-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eaa04-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eaa04-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eaa04-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eaa04-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="eaa04-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eaa04-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eaa04-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaa04-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaa04-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

