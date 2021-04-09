---
title: Mensaje de TVM_SETBORDER (commctrl. h)
description: Establece el tamaño del borde de los elementos de un control de vista de árbol. Puede enviar el mensaje explícitamente o mediante la \_ macro SetBorder de TreeView.
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- TVM_SETBORDER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4401959e2579caab7f2cb4b6eed1ea34481ffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905350"
---
# <a name="tvm_setborder-message"></a><span data-ttu-id="e4b38-105">\_Mensaje de SETBORDER TVM</span><span class="sxs-lookup"><span data-stu-id="e4b38-105">TVM\_SETBORDER message</span></span>

<span data-ttu-id="e4b38-106">**Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.**</span><span class="sxs-lookup"><span data-stu-id="e4b38-106">**Intended for internal use; not recommended for use in applications.**</span></span>

<span data-ttu-id="e4b38-107">Establece el tamaño del borde de los elementos de un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="e4b38-107">Sets the size of the border for the items in a tree-view control.</span></span> <span data-ttu-id="e4b38-108">Puede enviar el mensaje explícitamente o mediante la macro [**\_ SetBorder de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) .</span><span class="sxs-lookup"><span data-stu-id="e4b38-108">You can send the message explicitly or by using the [**TreeView\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4b38-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4b38-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b38-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4b38-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b38-111">Marcas de acción.</span><span class="sxs-lookup"><span data-stu-id="e4b38-111">Action flags.</span></span> <span data-ttu-id="e4b38-112">Este parámetro puede ser uno o varios de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e4b38-112">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="e4b38-113">Value</span><span class="sxs-lookup"><span data-stu-id="e4b38-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="e4b38-114">Significado</span><span class="sxs-lookup"><span data-stu-id="e4b38-114">Meaning</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <span data-ttu-id="e4b38-115"><dt>**TVSBF \_ XBORDER**</dt></span><span class="sxs-lookup"><span data-stu-id="e4b38-115"><dt>**TVSBF\_XBORDER**</dt></span></span> </dl> | <span data-ttu-id="e4b38-116">Aplica el tamaño de borde especificado al lado izquierdo de los elementos del control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="e4b38-116">Applies the specified border size to the left side of the items in the tree-view control.</span></span> <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <span data-ttu-id="e4b38-117"><dt>**TVSBF \_ YBORDER**</dt></span><span class="sxs-lookup"><span data-stu-id="e4b38-117"><dt>**TVSBF\_YBORDER**</dt></span></span> </dl> | <span data-ttu-id="e4b38-118">Aplica el tamaño de borde especificado a la parte superior de los elementos del control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="e4b38-118">Applies the specified border size to the top of the items in the tree-view control.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="e4b38-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4b38-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b38-120">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un **breve** que especifica el tamaño del borde izquierdo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e4b38-120">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **SHORT** that specifies the size of the left border, in pixels.</span></span> <span data-ttu-id="e4b38-121">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es un **breve** que especifica el tamaño del borde superior, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e4b38-121">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **SHORT** that specifies the size of the top border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b38-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4b38-122">Return value</span></span>

<span data-ttu-id="e4b38-123">Devuelve un valor **Long** que contiene el tamaño de borde anterior, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e4b38-123">Returns a **LONG** value that contains the previous border size, in pixels.</span></span> <span data-ttu-id="e4b38-124">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el tamaño anterior del borde horizontal y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene el tamaño anterior del borde vertical.</span><span class="sxs-lookup"><span data-stu-id="e4b38-124">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the previous size of the horizontal border, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the previous size of the vertical border.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b38-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4b38-125">Remarks</span></span>

<span data-ttu-id="e4b38-126">**Advertencia de seguridad:** El uso de este mensaje podría poner en peligro la seguridad del programa.</span><span class="sxs-lookup"><span data-stu-id="e4b38-126">**Security Warning:** Using this message might compromise the security of your program.</span></span>

<span data-ttu-id="e4b38-127">El borde del elemento se establece solo con fines de espaciado.</span><span class="sxs-lookup"><span data-stu-id="e4b38-127">The item border is set just for spacing purposes.</span></span> <span data-ttu-id="e4b38-128">Un valor correcto desencadena un recálculo de las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="e4b38-128">A successful setting triggers a recalculation of the scroll bars.</span></span>

<span data-ttu-id="e4b38-129">Es posible que este mensaje no se admita en versiones futuras de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="e4b38-129">This message may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="e4b38-130">Además, este mensaje no se define en commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="e4b38-130">Also, this message is not defined in commctrl.h.</span></span> <span data-ttu-id="e4b38-131">Agregue las siguientes definiciones a los archivos de origen de la aplicación para usar el mensaje:</span><span class="sxs-lookup"><span data-stu-id="e4b38-131">Add the following definitions to the source files of your application to use the message:</span></span>

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a><span data-ttu-id="e4b38-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4b38-132">Requirements</span></span>



| <span data-ttu-id="e4b38-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4b38-133">Requirement</span></span> | <span data-ttu-id="e4b38-134">Value</span><span class="sxs-lookup"><span data-stu-id="e4b38-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b38-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4b38-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b38-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e4b38-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4b38-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4b38-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b38-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4b38-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4b38-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4b38-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b38-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b38-140"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b38-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4b38-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b38-142">**SetBorder de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="e4b38-142">**TreeView\_SetBorder**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

