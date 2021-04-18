---
title: Mensaje de PGM_SETBUTTONSIZE (commctrl. h)
description: Establece el tamaño del botón actual para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro SetButtonSize de buscapersonas \_ .
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- PGM_SETBUTTONSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf8c164ed960675c1a68be36acfe0eff40f972f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534030"
---
# <a name="pgm_setbuttonsize-message"></a><span data-ttu-id="5b268-105">\_Mensaje SETBUTTONSIZE PGM</span><span class="sxs-lookup"><span data-stu-id="5b268-105">PGM\_SETBUTTONSIZE message</span></span>

<span data-ttu-id="5b268-106">Establece el tamaño del botón actual para el control de paginación.</span><span class="sxs-lookup"><span data-stu-id="5b268-106">Sets the current button size for the pager control.</span></span> <span data-ttu-id="5b268-107">Puede enviar este mensaje explícitamente o utilizar la macro [**\_ SetButtonSize de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) .</span><span class="sxs-lookup"><span data-stu-id="5b268-107">You can send this message explicitly or use the [**Pager\_SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b268-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b268-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b268-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b268-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5b268-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5b268-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5b268-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b268-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b268-112">Valor de tipo **int** que contiene el nuevo tamaño de botón, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="5b268-112">Value of type **int** that contains the new button size, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b268-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b268-113">Return value</span></span>

<span data-ttu-id="5b268-114">Devuelve un valor **int** que contiene el tamaño de botón anterior, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="5b268-114">Returns an **int** value that contains the previous button size, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b268-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b268-115">Remarks</span></span>

<span data-ttu-id="5b268-116">Si el control de paginación tiene el estilo [**págs \_ horizontal**](pager-control-styles.md) , el tamaño del botón determina el ancho de los botones de paginación.</span><span class="sxs-lookup"><span data-stu-id="5b268-116">If the pager control has the [**PGS\_HORZ**](pager-control-styles.md) style, the button size determines the width of the pager buttons.</span></span> <span data-ttu-id="5b268-117">Si el control de paginación tiene el estilo [**págs \_ Vert**](pager-control-styles.md) , el tamaño del botón determina el alto de los botones de paginación.</span><span class="sxs-lookup"><span data-stu-id="5b268-117">If the pager control has the [**PGS\_VERT**](pager-control-styles.md) style, the button size determines the height of the pager buttons.</span></span> <span data-ttu-id="5b268-118">De forma predeterminada, el control de paginación establece su tamaño de botón en tres cuartos del ancho de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="5b268-118">By default, the pager control sets its button size to three-fourths of the width of the scroll bar.</span></span>

<span data-ttu-id="5b268-119">Hay un tamaño mínimo para el botón de buscapersonas; actualmente, 12 píxeles.</span><span class="sxs-lookup"><span data-stu-id="5b268-119">There is a minimum size to the pager button, currently 12 pixels.</span></span> <span data-ttu-id="5b268-120">Sin embargo, esto puede cambiar, por lo que no debe depender de este valor.</span><span class="sxs-lookup"><span data-stu-id="5b268-120">However, this can change so you should not depend on this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b268-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b268-121">Requirements</span></span>



| <span data-ttu-id="5b268-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b268-122">Requirement</span></span> | <span data-ttu-id="5b268-123">Value</span><span class="sxs-lookup"><span data-stu-id="5b268-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b268-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b268-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5b268-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5b268-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b268-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b268-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5b268-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5b268-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b268-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b268-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b268-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b268-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b268-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b268-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b268-131">**\_GETBUTTONSIZE PGM**</span><span class="sxs-lookup"><span data-stu-id="5b268-131">**PGM\_GETBUTTONSIZE**</span></span>](pgm-getbuttonsize.md)
</dt> </dl>

 

 





