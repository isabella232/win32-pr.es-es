---
title: Mensaje de CB_GETMINVISIBLE (commctrl. h)
description: Obtiene el número mínimo de elementos visibles en la lista desplegable de un cuadro combinado.
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- CB_GETMINVISIBLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf4fe5088d9c994e232a64ba16bbddf11b0d48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905241"
---
# <a name="cb_getminvisible-message"></a><span data-ttu-id="15640-104">\_Mensaje GETMINVISIBLE CB</span><span class="sxs-lookup"><span data-stu-id="15640-104">CB\_GETMINVISIBLE message</span></span>

<span data-ttu-id="15640-105">Obtiene el número mínimo de elementos visibles en la lista desplegable de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="15640-105">Gets the minimum number of visible items in the drop-down list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="15640-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15640-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15640-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15640-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15640-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="15640-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="15640-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15640-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15640-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="15640-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15640-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15640-111">Return value</span></span>

<span data-ttu-id="15640-112">El valor devuelto es el número mínimo de elementos visibles.</span><span class="sxs-lookup"><span data-stu-id="15640-112">The return value is the minimum number of visible items.</span></span>

## <a name="remarks"></a><span data-ttu-id="15640-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15640-113">Remarks</span></span>

<span data-ttu-id="15640-114">Cuando el número de elementos de la lista desplegable es mayor que el mínimo, el cuadro combinado usa una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="15640-114">When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar.</span></span>

<span data-ttu-id="15640-115">Este mensaje se omite si el control de cuadro combinado tiene el estilo [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="15640-115">This message is ignored if the combo box control has style [**CBS\_NOINTEGRALHEIGHT**](combo-box-styles.md).</span></span>

<span data-ttu-id="15640-116">Para usar **CB \_ GETMINVISIBLE**, la aplicación debe especificar comctl32.dll versión 6 del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="15640-116">To use **CB\_GETMINVISIBLE**, the application must specify comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="15640-117">Para obtener más información, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="15640-117">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15640-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15640-118">Requirements</span></span>



| <span data-ttu-id="15640-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="15640-119">Requirement</span></span> | <span data-ttu-id="15640-120">Value</span><span class="sxs-lookup"><span data-stu-id="15640-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15640-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15640-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15640-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="15640-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="15640-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15640-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15640-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="15640-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="15640-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15640-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="15640-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="15640-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15640-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="15640-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="15640-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="15640-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="15640-129">**CB \_ SETMINVISIBLE**</span><span class="sxs-lookup"><span data-stu-id="15640-129">**CB\_SETMINVISIBLE**</span></span>](cb-setminvisible.md)
</dt> <dt>

[<span data-ttu-id="15640-130">**ComboBox \_ GetMinVisible**</span><span class="sxs-lookup"><span data-stu-id="15640-130">**ComboBox\_GetMinVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





