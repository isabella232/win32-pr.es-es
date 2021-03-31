---
title: Mensaje de LVM_SETCOLUMNWIDTH (commctrl. h)
description: Cambia el ancho de una columna en el modo de vista de informe o el ancho de todas las columnas en el modo de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetColumnWidth de ListView.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- LVM_SETCOLUMNWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529e989b3d66562acc7b6f91c3b3b06527235e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149899"
---
# <a name="lvm_setcolumnwidth-message"></a><span data-ttu-id="fda0a-105">\_Mensaje SETCOLUMNWIDTH LVM</span><span class="sxs-lookup"><span data-stu-id="fda0a-105">LVM\_SETCOLUMNWIDTH message</span></span>

<span data-ttu-id="fda0a-106">Cambia el ancho de una columna en el modo de vista de informe o el ancho de todas las columnas en el modo de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="fda0a-106">Changes the width of a column in report-view mode or the width of all columns in list-view mode.</span></span> <span data-ttu-id="fda0a-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetColumnWidth de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) .</span><span class="sxs-lookup"><span data-stu-id="fda0a-107">You can send this message explicitly or use the [**ListView\_SetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fda0a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fda0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fda0a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fda0a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fda0a-110">Índice de base cero de una columna válida.</span><span class="sxs-lookup"><span data-stu-id="fda0a-110">Zero-based index of a valid column.</span></span> <span data-ttu-id="fda0a-111">En el modo de vista de lista, este parámetro debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="fda0a-111">For list-view mode, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fda0a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fda0a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fda0a-113">Nuevo ancho de la columna, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fda0a-113">New width of the column, in pixels.</span></span> <span data-ttu-id="fda0a-114">En el modo de vista de informe, se admiten los siguientes valores especiales:</span><span class="sxs-lookup"><span data-stu-id="fda0a-114">For report-view mode, the following special values are supported:</span></span>



| <span data-ttu-id="fda0a-115">Value</span><span class="sxs-lookup"><span data-stu-id="fda0a-115">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="fda0a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="fda0a-116">Meaning</span></span>                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <span data-ttu-id="fda0a-117"><dt>**AutoSize de LVSCW \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fda0a-117"><dt>**LVSCW\_AUTOSIZE**</dt></span></span> </dl>                                | <span data-ttu-id="fda0a-118">Ajusta automáticamente el tamaño de la columna.</span><span class="sxs-lookup"><span data-stu-id="fda0a-118">Automatically sizes the column.</span></span><br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <span data-ttu-id="fda0a-119"><dt>**LVSCW \_ AutoSize \_ USEHEADER**</dt></span><span class="sxs-lookup"><span data-stu-id="fda0a-119"><dt>**LVSCW\_AUTOSIZE\_USEHEADER**</dt></span></span> </dl> | <span data-ttu-id="fda0a-120">Ajusta el tamaño de la columna automáticamente para que quepa el texto del encabezado.</span><span class="sxs-lookup"><span data-stu-id="fda0a-120">Automatically sizes the column to fit the header text.</span></span> <span data-ttu-id="fda0a-121">Si usa este valor con la última columna, su ancho se establece para rellenar el ancho restante del control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="fda0a-121">If you use this value with the last column, its width is set to fill the remaining width of the list-view control.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fda0a-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fda0a-122">Return value</span></span>

<span data-ttu-id="fda0a-123">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fda0a-123">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fda0a-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fda0a-124">Remarks</span></span>

<span data-ttu-id="fda0a-125">Suponga que tiene un control de vista de lista de 2 columnas con un ancho de 500 píxeles.</span><span class="sxs-lookup"><span data-stu-id="fda0a-125">Assume that you have a 2-column list-view control with a width of 500 pixels.</span></span> <span data-ttu-id="fda0a-126">Si el ancho de la columna cero se establece en 200 píxeles y se envía este mensaje con *wParam* = 1 y *lParam* = LVSCW \_ AutoSize \_ USEHEADER, la segunda columna (y la última) será de 300 píxeles de ancho.</span><span class="sxs-lookup"><span data-stu-id="fda0a-126">If the width of column zero is set to 200 pixels, and you send this message with *wParam* = 1 and *lParam* = LVSCW\_AUTOSIZE\_USEHEADER, the second (and last) column will be 300 pixels wide.</span></span>

## <a name="requirements"></a><span data-ttu-id="fda0a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fda0a-127">Requirements</span></span>



| <span data-ttu-id="fda0a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fda0a-128">Requirement</span></span> | <span data-ttu-id="fda0a-129">Value</span><span class="sxs-lookup"><span data-stu-id="fda0a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fda0a-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fda0a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fda0a-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fda0a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fda0a-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fda0a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fda0a-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fda0a-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fda0a-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fda0a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fda0a-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fda0a-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





