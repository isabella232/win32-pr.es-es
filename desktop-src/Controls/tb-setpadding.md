---
title: Mensaje de TB_SETPADDING (commctrl. h)
description: Establece el relleno de un control de barra de herramientas.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- TB_SETPADDING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65fae53f7e7702528915af7631bd675f11188b71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150976"
---
# <a name="tb_setpadding-message"></a><span data-ttu-id="b6bb6-104">\_Mensaje SETPADDING TB</span><span class="sxs-lookup"><span data-stu-id="b6bb6-104">TB\_SETPADDING message</span></span>

<span data-ttu-id="b6bb6-105">Establece el relleno de un control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-105">Sets the padding for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6bb6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6bb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6bb6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6bb6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6bb6-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b6bb6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6bb6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6bb6-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el relleno horizontal, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the horizontal padding, in pixels.</span></span> <span data-ttu-id="b6bb6-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el relleno vertical, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6bb6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6bb6-112">Return value</span></span>

<span data-ttu-id="b6bb6-113">Devuelve un valor **DWORD** que contiene el relleno horizontal anterior en el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y el relleno vertical anterior en el [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-113">Returns a **DWORD** value that contains the previous horizontal padding in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous vertical padding in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6bb6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6bb6-114">Remarks</span></span>

<span data-ttu-id="b6bb6-115">Los valores de relleno se usan para crear un área en blanco entre el borde del botón y la imagen o el texto del botón.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-115">The padding values are used to create a blank area between the edge of the button and the button's image and/or text.</span></span> <span data-ttu-id="b6bb6-116">Dónde y cuánto relleno se aplica realmente depende del tipo del botón y de si tiene una imagen.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-116">Where and how much padding is actually applied depends on the type of the button and whether it has an image.</span></span> <span data-ttu-id="b6bb6-117">El relleno horizontal se aplica a la derecha y a la izquierda del botón, y el relleno vertical se aplica a la parte superior e inferior del botón.</span><span class="sxs-lookup"><span data-stu-id="b6bb6-117">The horizontal padding is applied to both the right and left of the button, and the vertical padding is applied to both the top and bottom of the button.</span></span> <span data-ttu-id="b6bb6-118">El relleno solo se aplica a los botones que tienen el estilo de [**\_ ajuste automático de TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b6bb6-118">Padding is only applied to buttons that have the [**TBSTYLE\_AUTOSIZE**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6bb6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6bb6-119">Requirements</span></span>



| <span data-ttu-id="b6bb6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6bb6-120">Requirement</span></span> | <span data-ttu-id="b6bb6-121">Value</span><span class="sxs-lookup"><span data-stu-id="b6bb6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6bb6-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6bb6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b6bb6-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b6bb6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6bb6-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6bb6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b6bb6-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b6bb6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6bb6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6bb6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6bb6-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6bb6-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6bb6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6bb6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6bb6-129">**TB \_ GETPADDING**</span><span class="sxs-lookup"><span data-stu-id="b6bb6-129">**TB\_GETPADDING**</span></span>](tb-getpadding.md)
</dt> </dl>

 

