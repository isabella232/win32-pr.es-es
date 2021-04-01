---
title: Mensaje de EM_SETEXTENDEDSTYLE (commctrl. h)
description: Informa al control de edición para establecer los estilos extendidos. Envíe este mensaje o use la macro Edit \_ SetExtendedStyle.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- EM_SETEXTENDEDSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 560b675927b4497810b8d492fd89b5765aa5a2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150916"
---
# <a name="em_setextendedstyle-message"></a><span data-ttu-id="9cde2-105">\_Mensaje SETEXTENDEDSTYLE em</span><span class="sxs-lookup"><span data-stu-id="9cde2-105">EM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="9cde2-106">Informa al control de edición para establecer los estilos extendidos.</span><span class="sxs-lookup"><span data-stu-id="9cde2-106">Informs the edit control to set extended styles.</span></span> <span data-ttu-id="9cde2-107">Envíe este mensaje o use la macro [**Edit \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).</span><span class="sxs-lookup"><span data-stu-id="9cde2-107">Send this message or use the macro [**Edit\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="9cde2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9cde2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cde2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9cde2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cde2-110">Máscara que se usa para seleccionar los estilos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="9cde2-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="9cde2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9cde2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cde2-112">Valor que indica el estilo extendido.</span><span class="sxs-lookup"><span data-stu-id="9cde2-112">Value that indicates the extended style.</span></span> <span data-ttu-id="9cde2-113">Para obtener más información sobre los estilos, vea [Edit control Extended Styles](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="9cde2-113">For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cde2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9cde2-114">Return value</span></span>

<span data-ttu-id="9cde2-115">Si este mensaje se realiza correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9cde2-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9cde2-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9cde2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cde2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9cde2-117">Remarks</span></span>

<span data-ttu-id="9cde2-118">Los estilos extendidos para un control de edición no tienen nada que hacer con los estilos extendidos usados con la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="9cde2-118">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cde2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cde2-119">Requirements</span></span>



| <span data-ttu-id="9cde2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cde2-120">Requirement</span></span> | <span data-ttu-id="9cde2-121">Value</span><span class="sxs-lookup"><span data-stu-id="9cde2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9cde2-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cde2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9cde2-123">Solo aplicaciones de escritorio de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="9cde2-123">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9cde2-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cde2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9cde2-125">Solo aplicaciones de escritorio de Windows Server 2019 \[\]</span><span class="sxs-lookup"><span data-stu-id="9cde2-125">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9cde2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9cde2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cde2-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cde2-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

