---
title: Mensaje EM_SETTABLEPARMS (RichEdit. h)
description: Cambia los parámetros de las filas de una tabla.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- EM_SETTABLEPARMS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fa77774bd7fcf461fc74b479a57304a5f8ee3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996223"
---
# <a name="em_settableparms-message"></a><span data-ttu-id="45d70-104">\_Mensaje SETTABLEPARMS em</span><span class="sxs-lookup"><span data-stu-id="45d70-104">EM\_SETTABLEPARMS message</span></span>

<span data-ttu-id="45d70-105">Cambia los parámetros de las filas de una tabla.</span><span class="sxs-lookup"><span data-stu-id="45d70-105">Changes the parameters of rows in a table.</span></span>

## <a name="parameters"></a><span data-ttu-id="45d70-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45d70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45d70-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="45d70-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45d70-108">Puntero a una estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="45d70-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="45d70-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45d70-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45d70-110">Puntero a una estructura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="45d70-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45d70-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45d70-111">Return value</span></span>

<span data-ttu-id="45d70-112">Devuelve \_ si es correcto, o uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="45d70-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="45d70-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="45d70-113">Return code</span></span>                                                                                    | <span data-ttu-id="45d70-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="45d70-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45d70-115"><dt>**E \_ ERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="45d70-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="45d70-116">No se pueden realizar cambios.</span><span class="sxs-lookup"><span data-stu-id="45d70-116">Changes cannot be made.</span></span> <span data-ttu-id="45d70-117">Esto puede ocurrir si el control es un control de texto sin formato o de una sola línea, o si el punto de inserción está dentro de un objeto matemático.</span><span class="sxs-lookup"><span data-stu-id="45d70-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="45d70-118">También se produce si las tablas están deshabilitadas o si el mensaje [**em \_ SETEDITSTYLEEX**](em-seteditstyleex.md) establece el valor **\_ \_ importante de SES** .</span><span class="sxs-lookup"><span data-stu-id="45d70-118">It also occurs if tables are disabled, or if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="45d70-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="45d70-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="45d70-120">*WParam* o *lParam* es null o apunta a una estructura no válida.</span><span class="sxs-lookup"><span data-stu-id="45d70-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="45d70-121">El miembro **cCell** de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) debe ser al menos 1 y no superior a 63.</span><span class="sxs-lookup"><span data-stu-id="45d70-121">The **cCell** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must be at least 1 and not more than 63.</span></span> <span data-ttu-id="45d70-122">El miembro **cbRow** debe ser igual a `sizeof(TABLEROWPARMS)` o `sizeof(TABLEROWPARMS)   2*sizeof(long)` .</span><span class="sxs-lookup"><span data-stu-id="45d70-122">The **cbRow** member must equal `sizeof(TABLEROWPARMS)` or `sizeof(TABLEROWPARMS)   2*sizeof(long)`.</span></span> <span data-ttu-id="45d70-123">El último valor es el tamaño de la estructura **TABLEROWPARMS** de RichEdit 4,1.</span><span class="sxs-lookup"><span data-stu-id="45d70-123">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="45d70-124">El miembro **cbCell** de **TABLEROWPARMS** debe ser igual a `sizeof(TABLECELLPARMS)` .</span><span class="sxs-lookup"><span data-stu-id="45d70-124">The **cbCell** member of **TABLEROWPARMS** must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="45d70-125">El punto de inserción debe estar al principio de una tabla o dentro de una fila de la tabla, y el número de celdas solo puede cambiar en uno.</span><span class="sxs-lookup"><span data-stu-id="45d70-125">The insertion point must be at the start of a table or inside a table row, and the number of cells can only change by one.</span></span> |
| <dl> <span data-ttu-id="45d70-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="45d70-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="45d70-127">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="45d70-127">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="45d70-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45d70-128">Remarks</span></span>

<span data-ttu-id="45d70-129">Este mensaje cambia los parámetros del número de filas especificado por el miembro **cRow** de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) , si la tabla tiene tantas filas consecutivas.</span><span class="sxs-lookup"><span data-stu-id="45d70-129">This message changes the parameters of the number of rows specified by the **cRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, if the table has that many consecutive rows.</span></span> <span data-ttu-id="45d70-130">Si **cRow** es menor que 0, el mensaje se recorre en iteración hasta el final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="45d70-130">If **cRow** is less than 0, the message iterates until the end of the table.</span></span> <span data-ttu-id="45d70-131">Si el recuento de celdas nuevo difiere del número de celdas actual en + 1 o 1, inserta o elimina la celda en el índice especificado por el miembro **iCell** de **TABLEROWPARMS**.</span><span class="sxs-lookup"><span data-stu-id="45d70-131">If the new cell count differs from the current cell count by +1 or  1, it inserts or deletes the cell at the index specified by the **iCell** member of **TABLEROWPARMS**.</span></span> <span data-ttu-id="45d70-132">La fila de la tabla inicial se identifica mediante una posición de carácter.</span><span class="sxs-lookup"><span data-stu-id="45d70-132">The starting table row is identified by a character position.</span></span> <span data-ttu-id="45d70-133">Esta posición se especifica mediante miembros **cpStartRow** con valores que son mayores o iguales que cero.</span><span class="sxs-lookup"><span data-stu-id="45d70-133">This position is specified by **cpStartRow** members with values that are greater than or equal to zero.</span></span> <span data-ttu-id="45d70-134">La posición debe estar dentro de la fila de la tabla, pero no dentro de una tabla anidada, a menos que desee cambiar los parámetros de la tabla s.</span><span class="sxs-lookup"><span data-stu-id="45d70-134">The position should be inside the table row, but not inside a nested table, unless you want to change that table s parameters.</span></span> <span data-ttu-id="45d70-135">Si el miembro **cpStartRow** es 1, la selección actual proporciona la posición del carácter.</span><span class="sxs-lookup"><span data-stu-id="45d70-135">If the **cpStartRow** member is  1, the character position is given by the current selection.</span></span> <span data-ttu-id="45d70-136">Para ello, coloque la selección en cualquier lugar dentro de la fila de la tabla o seleccione la fila con el extremo activo de la selección al final de la fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="45d70-136">For this, position the selection anywhere inside the table row, or select the row with the active end of the selection at the end of the table row.</span></span>

## <a name="requirements"></a><span data-ttu-id="45d70-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45d70-137">Requirements</span></span>



| <span data-ttu-id="45d70-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="45d70-138">Requirement</span></span> | <span data-ttu-id="45d70-139">Value</span><span class="sxs-lookup"><span data-stu-id="45d70-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45d70-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45d70-140">Minimum supported client</span></span><br/> | <span data-ttu-id="45d70-141">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="45d70-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="45d70-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45d70-142">Minimum supported server</span></span><br/> | <span data-ttu-id="45d70-143">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="45d70-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45d70-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45d70-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="45d70-145"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="45d70-145"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45d70-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="45d70-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d70-147">**\_GETTABLEPARMS em**</span><span class="sxs-lookup"><span data-stu-id="45d70-147">**EM\_GETTABLEPARMS**</span></span>](em-gettableparms.md)
</dt> </dl>

 

 





