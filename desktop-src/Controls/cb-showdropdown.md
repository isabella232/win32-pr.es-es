---
title: Mensaje de CB_SHOWDROPDOWN (Winuser. h)
description: Una aplicación envía un \_ mensaje CB SHOWDROPDOWN para mostrar u ocultar el cuadro de lista de un cuadro combinado que tenga el \_ estilo desplegable CBS o CBS \_ DROPDOWNLIST.
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- CB_SHOWDROPDOWN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150927"
---
# <a name="cb_showdropdown-message"></a><span data-ttu-id="5b2f9-104">\_Mensaje SHOWDROPDOWN CB</span><span class="sxs-lookup"><span data-stu-id="5b2f9-104">CB\_SHOWDROPDOWN message</span></span>

<span data-ttu-id="5b2f9-105">Una aplicación envía un mensaje **CB \_ SHOWDROPDOWN** para mostrar u ocultar el cuadro de lista de un cuadro combinado que tenga el estilo [**\_ desplegable CBS**](combo-box-styles.md) o [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5b2f9-105">An application sends a **CB\_SHOWDROPDOWN** message to show or hide the list box of a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b2f9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b2f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b2f9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b2f9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b2f9-108">Un **booleano** que especifica si se va a mostrar u ocultar el cuadro de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="5b2f9-108">A **BOOL** that specifies whether the drop-down list box is to be shown or hidden.</span></span> <span data-ttu-id="5b2f9-109">Un valor de **true** muestra el cuadro de lista; un valor **false** lo oculta.</span><span class="sxs-lookup"><span data-stu-id="5b2f9-109">A value of **TRUE** shows the list box; a value of **FALSE** hides it.</span></span>

</dd> <dt>

<span data-ttu-id="5b2f9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b2f9-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b2f9-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5b2f9-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b2f9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b2f9-112">Return value</span></span>

<span data-ttu-id="5b2f9-113">El valor devuelto siempre es **true**.</span><span class="sxs-lookup"><span data-stu-id="5b2f9-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b2f9-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b2f9-114">Remarks</span></span>

<span data-ttu-id="5b2f9-115">Este mensaje no tiene ningún efecto en un cuadro combinado creado con el estilo [**\_ simple CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5b2f9-115">This message has no effect on a combo box created with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b2f9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b2f9-116">Requirements</span></span>



| <span data-ttu-id="5b2f9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b2f9-117">Requirement</span></span> | <span data-ttu-id="5b2f9-118">Value</span><span class="sxs-lookup"><span data-stu-id="5b2f9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b2f9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b2f9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5b2f9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5b2f9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5b2f9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b2f9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5b2f9-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5b2f9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b2f9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b2f9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b2f9-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b2f9-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b2f9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b2f9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b2f9-126">**CB \_ GETDROPPEDSTATE**</span><span class="sxs-lookup"><span data-stu-id="5b2f9-126">**CB\_GETDROPPEDSTATE**</span></span>](cb-getdroppedstate.md)
</dt> </dl>

 

 





