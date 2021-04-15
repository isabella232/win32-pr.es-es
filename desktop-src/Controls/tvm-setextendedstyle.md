---
title: Mensaje de TVM_SETEXTENDEDSTYLE (commctrl. h)
description: Informa al control de vista de árbol para establecer los estilos extendidos. Envíe este mensaje o use la macro TreeView \_ SetExtendedStyle.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- TVM_SETEXTENDEDSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534342"
---
# <a name="tvm_setextendedstyle-message"></a><span data-ttu-id="21c41-105">\_Mensaje de SETEXTENDEDSTYLE TVM</span><span class="sxs-lookup"><span data-stu-id="21c41-105">TVM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="21c41-106">Informa al control de vista de árbol para establecer los estilos extendidos.</span><span class="sxs-lookup"><span data-stu-id="21c41-106">Informs the tree-view control to set extended styles.</span></span> <span data-ttu-id="21c41-107">Envíe este mensaje o use la macro [**TreeView \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).</span><span class="sxs-lookup"><span data-stu-id="21c41-107">Send this message or use the macro [**TreeView\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="21c41-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21c41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21c41-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="21c41-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21c41-110">Máscara que se usa para seleccionar los estilos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="21c41-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="21c41-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21c41-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21c41-112">Valor que indica el estilo extendido.</span><span class="sxs-lookup"><span data-stu-id="21c41-112">Value that indicates the extended style.</span></span> <span data-ttu-id="21c41-113">Para obtener más información sobre los estilos, vea los [estilos extendidos del control de vista de árbol](tree-view-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="21c41-113">For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21c41-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21c41-114">Return value</span></span>

<span data-ttu-id="21c41-115">Si este mensaje se realiza correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="21c41-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21c41-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21c41-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="21c41-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21c41-117">Remarks</span></span>

<span data-ttu-id="21c41-118">Los estilos extendidos para un control de vista de árbol no tienen nada que ver con los estilos extendidos que se usan con la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="21c41-118">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="21c41-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21c41-119">Requirements</span></span>



| <span data-ttu-id="21c41-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="21c41-120">Requirement</span></span> | <span data-ttu-id="21c41-121">Value</span><span class="sxs-lookup"><span data-stu-id="21c41-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21c41-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21c41-122">Minimum supported client</span></span><br/> | <span data-ttu-id="21c41-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="21c41-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21c41-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21c41-124">Minimum supported server</span></span><br/> | <span data-ttu-id="21c41-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="21c41-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21c41-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21c41-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="21c41-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="21c41-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

