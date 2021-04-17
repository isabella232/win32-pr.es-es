---
title: Mensaje de CB_SETEXTENDEDUI (Winuser. h)
description: Una aplicación envía un \_ mensaje CB SETEXTENDEDUI para seleccionar la interfaz de usuario predeterminada o la interfaz de usuario extendida para un cuadro combinado que tenga el estilo de la \_ lista desplegable CBS o CBS \_ DROPDOWNLIST.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- CB_SETEXTENDEDUI controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94c31c8bc5457799d0038ecd8340c03c55aed91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490528"
---
# <a name="cb_setextendedui-message"></a><span data-ttu-id="bb282-104">\_Mensaje SETEXTENDEDUI CB</span><span class="sxs-lookup"><span data-stu-id="bb282-104">CB\_SETEXTENDEDUI message</span></span>

<span data-ttu-id="bb282-105">Una aplicación envía un mensaje **CB \_ SETEXTENDEDUI** para seleccionar la interfaz de usuario predeterminada o la interfaz de usuario extendida para un cuadro combinado que tenga el estilo de la [**\_ lista desplegable CBS**](combo-box-styles.md) o [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="bb282-105">An application sends a **CB\_SETEXTENDEDUI** message to select either the default UI or the extended UI for a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb282-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb282-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb282-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb282-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb282-108">Un valor **booleano** que especifica si el cuadro combinado usa la interfaz de usuario extendida (**true**) o la interfaz de usuario predeterminada (**false**).</span><span class="sxs-lookup"><span data-stu-id="bb282-108">A **BOOL** that specifies whether the combo box uses the extended UI (**TRUE**) or the default UI (**FALSE**).</span></span>

</dd> <dt>

<span data-ttu-id="bb282-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb282-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb282-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bb282-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb282-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb282-111">Return value</span></span>

<span data-ttu-id="bb282-112">Si la operación se realiza correctamente, el valor devuelto es CB de \_ acuerdo.</span><span class="sxs-lookup"><span data-stu-id="bb282-112">If the operation succeeds, the return value is CB\_OKAY.</span></span> <span data-ttu-id="bb282-113">Si se produce un error, es CB \_ error.</span><span class="sxs-lookup"><span data-stu-id="bb282-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb282-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb282-114">Remarks</span></span>

<span data-ttu-id="bb282-115">De forma predeterminada, la tecla F4 abre o cierra la lista y la flecha hacia abajo cambia la selección actual.</span><span class="sxs-lookup"><span data-stu-id="bb282-115">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="bb282-116">En la interfaz de usuario extendida, la tecla F4 está deshabilitada y la tecla flecha abajo abre la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="bb282-116">In the extended UI, the F4 key is disabled and the DOWN ARROW key opens the drop-down list.</span></span> <span data-ttu-id="bb282-117">La rueda del mouse, que normalmente se desplaza por los elementos de la lista, no tiene ningún efecto cuando se establece la interfaz de usuario extendida.</span><span class="sxs-lookup"><span data-stu-id="bb282-117">The mouse wheel, which normally scrolls through the items in the list, has no effect when the extended UI is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb282-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb282-118">Requirements</span></span>



| <span data-ttu-id="bb282-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb282-119">Requirement</span></span> | <span data-ttu-id="bb282-120">Value</span><span class="sxs-lookup"><span data-stu-id="bb282-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb282-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb282-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bb282-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bb282-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bb282-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb282-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bb282-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb282-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bb282-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb282-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb282-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb282-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb282-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb282-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb282-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="bb282-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bb282-129">**CB \_ GETEXTENDEDUI**</span><span class="sxs-lookup"><span data-stu-id="bb282-129">**CB\_GETEXTENDEDUI**</span></span>](cb-getextendedui.md)
</dt> <dt>

<span data-ttu-id="bb282-130">**Vista**</span><span class="sxs-lookup"><span data-stu-id="bb282-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bb282-131">Características del cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="bb282-131">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





