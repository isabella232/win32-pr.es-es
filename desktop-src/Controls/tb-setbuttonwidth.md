---
title: Mensaje de TB_SETBUTTONWIDTH (commctrl. h)
description: Establece los anchos de botón mínimo y máximo en el control de barra de herramientas.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- TB_SETBUTTONWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150312"
---
# <a name="tb_setbuttonwidth-message"></a><span data-ttu-id="4e2de-104">\_Mensaje SETBUTTONWIDTH TB</span><span class="sxs-lookup"><span data-stu-id="4e2de-104">TB\_SETBUTTONWIDTH message</span></span>

<span data-ttu-id="4e2de-105">Establece los anchos de botón mínimo y máximo en el control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="4e2de-105">Sets the minimum and maximum button widths in the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e2de-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e2de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e2de-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e2de-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e2de-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4e2de-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4e2de-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e2de-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e2de-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el ancho mínimo del botón, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4e2de-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum button width, in pixels.</span></span> <span data-ttu-id="4e2de-111">Los botones de la barra de herramientas nunca serán más estrechos que este valor.</span><span class="sxs-lookup"><span data-stu-id="4e2de-111">Toolbar buttons will never be narrower than this value.</span></span>

<span data-ttu-id="4e2de-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el ancho máximo del botón, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4e2de-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum button width, in pixels.</span></span> <span data-ttu-id="4e2de-113">Si el texto del botón es demasiado ancho, el control lo muestra con puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="4e2de-113">If button text is too wide, the control displays it with ellipsis points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e2de-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e2de-114">Return value</span></span>

<span data-ttu-id="4e2de-115">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="4e2de-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e2de-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e2de-116">Remarks</span></span>

<span data-ttu-id="4e2de-117">Use **TB \_ SETBUTTONWIDTH** para establecer los anchos máximo y mínimo permitidos para los botones antes de agregarlos.</span><span class="sxs-lookup"><span data-stu-id="4e2de-117">Use **TB\_SETBUTTONWIDTH** to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="4e2de-118">Use [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) para establecer el tamaño real de los botones.</span><span class="sxs-lookup"><span data-stu-id="4e2de-118">Use [**TB\_SETBUTTONSIZE**](tb-setbuttonsize.md) to set the actual size of buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e2de-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e2de-119">Requirements</span></span>



| <span data-ttu-id="4e2de-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e2de-120">Requirement</span></span> | <span data-ttu-id="4e2de-121">Value</span><span class="sxs-lookup"><span data-stu-id="4e2de-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e2de-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e2de-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4e2de-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4e2de-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e2de-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e2de-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4e2de-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e2de-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e2de-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e2de-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e2de-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e2de-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

