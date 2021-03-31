---
title: Mensaje de CB_SETMINVISIBLE (commctrl. h)
description: Una aplicación envía un \_ mensaje CB SETMINVISIBLE para establecer el número mínimo de elementos visibles en la lista desplegable de un cuadro combinado.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- CB_SETMINVISIBLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac88155424c0b1ecf6c91f398e7a9a2d437eff90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149946"
---
# <a name="cb_setminvisible-message"></a><span data-ttu-id="32838-104">\_Mensaje SETMINVISIBLE CB</span><span class="sxs-lookup"><span data-stu-id="32838-104">CB\_SETMINVISIBLE message</span></span>

<span data-ttu-id="32838-105">Una aplicación envía un mensaje **CB \_ SETMINVISIBLE** para establecer el número mínimo de elementos visibles en la lista desplegable de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="32838-105">An application sends a **CB\_SETMINVISIBLE** message to set the minimum number of visible items in the drop-down list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="32838-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32838-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32838-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32838-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32838-108">Especifica el número mínimo de elementos visibles.</span><span class="sxs-lookup"><span data-stu-id="32838-108">Specifies the minimum number of visible items.</span></span>

</dd> <dt>

<span data-ttu-id="32838-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32838-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32838-110">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="32838-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32838-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32838-111">Return value</span></span>

<span data-ttu-id="32838-112">Si el mensaje se realiza correctamente, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="32838-112">If the message is successful, the return value is **TRUE**.</span></span> <span data-ttu-id="32838-113">De lo contrario, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="32838-113">Otherwise the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="32838-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32838-114">Remarks</span></span>

<span data-ttu-id="32838-115">Cuando el número de elementos de la lista desplegable es mayor que el mínimo, el cuadro combinado usa una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="32838-115">When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar.</span></span> <span data-ttu-id="32838-116">De forma predeterminada, 30 es el número mínimo de elementos visibles.</span><span class="sxs-lookup"><span data-stu-id="32838-116">By default, 30 is the minimum number of visible items.</span></span>

<span data-ttu-id="32838-117">Este mensaje se omite si el control de cuadro combinado tiene el estilo [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="32838-117">This message is ignored if the combo box control has style [**CBS\_NOINTEGRALHEIGHT**](combo-box-styles.md).</span></span>

<span data-ttu-id="32838-118">Para usar **CB \_ SETMINVISIBLE**, la aplicación debe especificar comctl32.dll versión 6 del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="32838-118">To use **CB\_SETMINVISIBLE**, the application must specify comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="32838-119">Para obtener más información, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="32838-119">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32838-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32838-120">Requirements</span></span>



| <span data-ttu-id="32838-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="32838-121">Requirement</span></span> | <span data-ttu-id="32838-122">Value</span><span class="sxs-lookup"><span data-stu-id="32838-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32838-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32838-123">Minimum supported client</span></span><br/> | <span data-ttu-id="32838-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="32838-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32838-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32838-125">Minimum supported server</span></span><br/> | <span data-ttu-id="32838-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="32838-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32838-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32838-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="32838-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="32838-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32838-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="32838-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="32838-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="32838-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="32838-131">**CB \_ GETMINVISIBLE**</span><span class="sxs-lookup"><span data-stu-id="32838-131">**CB\_GETMINVISIBLE**</span></span>](cb-getminvisible.md)
</dt> <dt>

[<span data-ttu-id="32838-132">**ComboBox \_ SetMinVisible**</span><span class="sxs-lookup"><span data-stu-id="32838-132">**ComboBox\_SetMinVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





