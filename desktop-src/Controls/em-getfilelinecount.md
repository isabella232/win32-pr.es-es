---
title: Mensaje de EM_GETFILELINECOUNT (CommCtrl. h)
description: Obtiene el número de líneas de un control de edición de varias líneas, independientemente de cómo se muestran las líneas en la pantalla.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETFILELINECOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETFILELINECOUNT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: bf48b3abeb10b98bf0c22a7dd2ef93c73a2a59c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150670"
---
# <a name="em_getfilelinecount-message-commctrlh"></a><span data-ttu-id="38900-104">Mensaje de EM_GETFILELINECOUNT (CommCtrl. h)</span><span class="sxs-lookup"><span data-stu-id="38900-104">EM_GETFILELINECOUNT message (CommCtrl.h)</span></span>

<span data-ttu-id="38900-105">Obtiene el número de líneas de un control de edición de varias líneas, independientemente de cómo se muestran las líneas en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="38900-105">Gets the number of lines in a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="38900-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38900-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38900-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38900-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38900-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="38900-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="38900-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38900-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38900-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="38900-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38900-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38900-111">Return value</span></span>

<span data-ttu-id="38900-112">El valor devuelto es un entero que especifica el número total de líneas de texto en el control de edición de varias líneas, independientemente de cómo se muestren las líneas en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="38900-112">The return value is an integer specifying the total number of text lines in the multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="38900-113">Si el control no tiene texto, el valor devuelto es 1.</span><span class="sxs-lookup"><span data-stu-id="38900-113">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="38900-114">El valor devuelto nunca será menor que 1.</span><span class="sxs-lookup"><span data-stu-id="38900-114">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="38900-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38900-115">Remarks</span></span>

<span data-ttu-id="38900-116">El **mensaje \_ GETFILELINECOUNT em** recupera el número total de líneas de texto, independientemente de cómo se muestren las líneas en la pantalla, no solo el número de líneas que están visibles actualmente.</span><span class="sxs-lookup"><span data-stu-id="38900-116">The **EM\_GETFILELINECOUNT** message retrieves the total number of text lines, independently of how lines are displayed on the screen, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="38900-117">El ajuste automático de línea no cambia el número de líneas que devuelve este mensaje, ya que este mensaje funciona independientemente del modo en que se muestran las líneas en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="38900-117">Word-wrap does not change the number of lines this message returns, as this message works independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="38900-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38900-118">Requirements</span></span>



| <span data-ttu-id="38900-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="38900-119">Requirement</span></span> | <span data-ttu-id="38900-120">Value</span><span class="sxs-lookup"><span data-stu-id="38900-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38900-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38900-121">Minimum supported client</span></span><br/> | <span data-ttu-id="38900-122">Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="38900-122">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="38900-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38900-123">Minimum supported server</span></span><br/> | <span data-ttu-id="38900-124">Solo aplicaciones de escritorio de Windows Server 2019 \[\]</span><span class="sxs-lookup"><span data-stu-id="38900-124">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="38900-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38900-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="38900-126"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="38900-126"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38900-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="38900-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="38900-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="38900-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="38900-129">**\_GETFILELINE em**</span><span class="sxs-lookup"><span data-stu-id="38900-129">**EM\_GETFILELINE**</span></span>](em-getfileline.md)
</dt> <dt>

[<span data-ttu-id="38900-130">**\_FILELINELENGTH em**</span><span class="sxs-lookup"><span data-stu-id="38900-130">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="38900-131">**Editar \_ GetFileLineCount**</span><span class="sxs-lookup"><span data-stu-id="38900-131">**Edit\_GetFileLineCount**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





