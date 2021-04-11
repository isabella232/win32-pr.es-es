---
title: Mensaje de CCM_DPISCALE (commctrl. h)
description: Habilita el escalado automático de puntos por pulgada (PPP) en controles Tree-View, controles de List-View, controles ComboBoxEx, controles de encabezado, botones, controles de barra de herramientas, controles de animación y listas de imágenes.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- CCM_DPISCALE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150565"
---
# <a name="ccm_dpiscale-message"></a><span data-ttu-id="214fd-104">\_Mensaje DPISCALE de CCM</span><span class="sxs-lookup"><span data-stu-id="214fd-104">CCM\_DPISCALE message</span></span>

<span data-ttu-id="214fd-105">Habilita el ajuste de escala automático de puntos por pulgada (PPP) en [controles de vista de árbol](tree-view-controls.md), [controles de vista de lista](list-view-control-reference.md), [controles ComboBoxEx](comboboxex-controls.md), [controles de encabezado](header-controls.md), [botones](buttons.md), controles de [barra de herramientas](toolbar-controls-overview.md), controles de [animación](animation-control-overview.md)y [listas de imágenes](image-lists.md).</span><span class="sxs-lookup"><span data-stu-id="214fd-105">Enables automatic high dots per inch (dpi) scaling in [Tree-View controls](tree-view-controls.md), [List-View controls](list-view-control-reference.md), [ComboBoxEx controls](comboboxex-controls.md), [Header controls](header-controls.md), [Buttons](buttons.md), [Toolbar controls](toolbar-controls-overview.md), [Animation controls](animation-control-overview.md), and [Image Lists](image-lists.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="214fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="214fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="214fd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="214fd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="214fd-108">Establézcalo en **true**.</span><span class="sxs-lookup"><span data-stu-id="214fd-108">Set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="214fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="214fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="214fd-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="214fd-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="214fd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="214fd-111">Return value</span></span>

<span data-ttu-id="214fd-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="214fd-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="214fd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="214fd-113">Remarks</span></span>

<span data-ttu-id="214fd-114">El inicio rápido y la [barra de tareas](/windows/desktop/shell/taskbar) no deben especificar un ajuste de escala de PPP, ya que las imágenes ya se han escalado.</span><span class="sxs-lookup"><span data-stu-id="214fd-114">Quick Launch and [Taskbar](/windows/desktop/shell/taskbar) should not specify a dpi scaling, because the images are already scaled.</span></span>

<span data-ttu-id="214fd-115">Cualquier control que utiliza una lista de imágenes creada con la métrica SmallIcon no debe escalar sus iconos.</span><span class="sxs-lookup"><span data-stu-id="214fd-115">Any control that uses an image list created with the SmallIcon metric should not scale its icons.</span></span>

> [!Note]  
> <span data-ttu-id="214fd-116">Para usar esta API, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="214fd-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="214fd-117">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="214fd-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="214fd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="214fd-118">Requirements</span></span>



| <span data-ttu-id="214fd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="214fd-119">Requirement</span></span> | <span data-ttu-id="214fd-120">Value</span><span class="sxs-lookup"><span data-stu-id="214fd-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="214fd-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="214fd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="214fd-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="214fd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="214fd-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="214fd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="214fd-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="214fd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="214fd-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="214fd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="214fd-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="214fd-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

