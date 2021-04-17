---
title: Mensaje de TVM_SETAUTOSCROLLINFO (commctrl. h)
description: Establece la información utilizada para determinar las características de desplazamiento automático. Puede enviar este mensaje explícitamente o mediante la \_ macro SetAutoScrollInfo de TreeView.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- TVM_SETAUTOSCROLLINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETAUTOSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa1f7920d2ec8c443b2ec5f1ff9189c22c5f21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656515"
---
# <a name="tvm_setautoscrollinfo-message"></a><span data-ttu-id="1508e-105">\_Mensaje de SETAUTOSCROLLINFO TVM</span><span class="sxs-lookup"><span data-stu-id="1508e-105">TVM\_SETAUTOSCROLLINFO message</span></span>

<span data-ttu-id="1508e-106">Establece la información utilizada para determinar las características de desplazamiento automático.</span><span class="sxs-lookup"><span data-stu-id="1508e-106">Sets information used to determine auto-scroll characteristics.</span></span> <span data-ttu-id="1508e-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetAutoScrollInfo de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="1508e-107">You can send this message explicitly or by using the [**TreeView\_SetAutoScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1508e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1508e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1508e-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1508e-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1508e-110">Especifica los píxeles por segundo.</span><span class="sxs-lookup"><span data-stu-id="1508e-110">Specifies pixels per second.</span></span> <span data-ttu-id="1508e-111">El desplazamiento que se va a desplazar se divide por el *wParam* para determinar la duración total del desplazamiento automático.</span><span class="sxs-lookup"><span data-stu-id="1508e-111">The offset to scroll is divided by the *wParam* to determine the total duration of the auto-scroll.</span></span>

</dd> <dt>

<span data-ttu-id="1508e-112">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1508e-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1508e-113">Especifica el intervalo de tiempo de redibujo.</span><span class="sxs-lookup"><span data-stu-id="1508e-113">Specifies the redraw time interval.</span></span> <span data-ttu-id="1508e-114">Vuelva a dibujar en cada intervalo de ELASPED hasta que el elemento se desplace en la vista.</span><span class="sxs-lookup"><span data-stu-id="1508e-114">Redraw at every elasped interval, until the item is scrolled into view.</span></span> <span data-ttu-id="1508e-115">Dado *wParam*, se calcula la ubicación del elemento y se produce un Repaint.</span><span class="sxs-lookup"><span data-stu-id="1508e-115">Given *wParam*, the location of the item is calculated and a repaint occurs.</span></span> <span data-ttu-id="1508e-116">Establezca este valor en crear desplazamiento suave.</span><span class="sxs-lookup"><span data-stu-id="1508e-116">Set this value to create smooth scrolling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1508e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1508e-117">Return value</span></span>

<span data-ttu-id="1508e-118">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="1508e-118">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1508e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1508e-119">Remarks</span></span>

<span data-ttu-id="1508e-120">La información de desplazamiento automático se utiliza para desplazarse por un elemento no visible en la vista.</span><span class="sxs-lookup"><span data-stu-id="1508e-120">Autoscroll information is used to scroll a nonvisible item into view.</span></span> <span data-ttu-id="1508e-121">El control debe tener el estilo extendido [**TV \_ ex \_ AUTOHSCROLL**](tree-view-control-window-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1508e-121">The control must have the [**TVS\_EX\_AUTOHSCROLL**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="1508e-122">Para obtener información sobre los estilos extendidos, vea Tree-View control Extended Styles.</span><span class="sxs-lookup"><span data-stu-id="1508e-122">For information on extended styles, see Tree-View Control Extended Styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="1508e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1508e-123">Requirements</span></span>



| <span data-ttu-id="1508e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1508e-124">Requirement</span></span> | <span data-ttu-id="1508e-125">Value</span><span class="sxs-lookup"><span data-stu-id="1508e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1508e-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1508e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1508e-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1508e-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1508e-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1508e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1508e-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1508e-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1508e-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1508e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1508e-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1508e-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





