---
title: Mensaje EM_GETTABLEPARMS (RichEdit. h)
description: Recupera los parámetros de tabla para una fila de tabla y los parámetros de celda para el número de celdas especificado.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- EM_GETTABLEPARMS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eb244b64258b1cf83559e21affea51b1d0c5d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905199"
---
# <a name="em_gettableparms-message"></a><span data-ttu-id="a6836-104">\_Mensaje GETTABLEPARMS em</span><span class="sxs-lookup"><span data-stu-id="a6836-104">EM\_GETTABLEPARMS message</span></span>

<span data-ttu-id="a6836-105">Recupera los parámetros de tabla para una fila de tabla y los parámetros de celda para el número de celdas especificado.</span><span class="sxs-lookup"><span data-stu-id="a6836-105">Retrieves the table parameters for a table row and the cell parameters for the specified number of cells.</span></span>


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



## <a name="parameters"></a><span data-ttu-id="a6836-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6836-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6836-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6836-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6836-108">Puntero a una estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="a6836-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a6836-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6836-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6836-110">Puntero a una estructura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="a6836-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6836-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6836-111">Return value</span></span>

<span data-ttu-id="a6836-112">Devuelve \_ si es correcto, o uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="a6836-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="a6836-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a6836-113">Return code</span></span>                                                                                    | <span data-ttu-id="a6836-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6836-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6836-115"><dt>**E \_ ERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="a6836-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="a6836-116">No se pueden realizar cambios.</span><span class="sxs-lookup"><span data-stu-id="a6836-116">Changes cannot be made.</span></span> <span data-ttu-id="a6836-117">Esto puede ocurrir si el control es un control de texto sin formato o de una sola línea, o si el punto de inserción está dentro de un objeto matemático.</span><span class="sxs-lookup"><span data-stu-id="a6836-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="a6836-118">También se produce si las tablas están deshabilitadas si el mensaje [**em \_ SETEDITSTYLEEX**](em-seteditstyleex.md) establece el valor **\_ \_ importante de SES** .</span><span class="sxs-lookup"><span data-stu-id="a6836-118">It also occurs if tables are disabled if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="a6836-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a6836-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="a6836-120">*WParam* o *lParam* es null o apunta a una estructura no válida.</span><span class="sxs-lookup"><span data-stu-id="a6836-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="a6836-121">El miembro **cbRow** de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) debe ser igual `sizeof(TABLEROWPARMS)` o sizeof (TABLEROWPARMS) 2 \* sizeof (Long).</span><span class="sxs-lookup"><span data-stu-id="a6836-121">The **cbRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must equal `sizeof(TABLEROWPARMS)` or sizeof(TABLEROWPARMS)   2\*sizeof(long).</span></span> <span data-ttu-id="a6836-122">El último valor es el tamaño de la estructura **TABLEROWPARMS** de RichEdit 4,1.</span><span class="sxs-lookup"><span data-stu-id="a6836-122">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="a6836-123">El miembro **cbCell** de la estructura **TABLEROWPARMS** debe ser igual a `sizeof(TABLECELLPARMS)` .</span><span class="sxs-lookup"><span data-stu-id="a6836-123">The **cbCell** member of the **TABLEROWPARMS** structure must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="a6836-124">La posición del carácter de la consulta debe estar en un delimitador de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="a6836-124">The query character position must be at a table row delimiter.</span></span> |
| <dl> <span data-ttu-id="a6836-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a6836-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="a6836-126">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="a6836-126">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="a6836-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6836-127">Remarks</span></span>

<span data-ttu-id="a6836-128">Este mensaje obtiene los parámetros de tabla para la fila en la posición de caracteres especificada por el miembro **cpStartRow** de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) y el número de celdas especificadas por el miembro **cCells** de la estructura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="a6836-128">This message gets the table parameters for the row at the character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, and the number of cells specified by the **cCells** member of the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

<span data-ttu-id="a6836-129">La posición de caracteres especificada por el miembro **cpStartRow** de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) debe estar al principio de la fila de la tabla o en el delimitador final de la fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="a6836-129">The character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure should be at the start of the table row, or at the end delimiter of the table row.</span></span> <span data-ttu-id="a6836-130">Si **cpStartRow** se establece en 1, la selección actual proporciona la posición del carácter.</span><span class="sxs-lookup"><span data-stu-id="a6836-130">If **cpStartRow** is set to  1, the character position is given by the current selection.</span></span> <span data-ttu-id="a6836-131">En este caso, coloque la selección al final de la fila (entre la marca de celda y el delimitador final de la fila de la tabla) o seleccione la fila.</span><span class="sxs-lookup"><span data-stu-id="a6836-131">In this case, position the selection at the end of the row (between the cell mark and the end delimiter of the table row), or select the row.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6836-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6836-132">Requirements</span></span>



| <span data-ttu-id="a6836-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6836-133">Requirement</span></span> | <span data-ttu-id="a6836-134">Value</span><span class="sxs-lookup"><span data-stu-id="a6836-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6836-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6836-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a6836-136">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6836-136">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a6836-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6836-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a6836-138">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6836-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6836-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6836-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6836-140"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6836-140"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6836-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6836-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6836-142">**\_SETTABLEPARMS em**</span><span class="sxs-lookup"><span data-stu-id="a6836-142">**EM\_SETTABLEPARMS**</span></span>](em-settableparms.md)
</dt> </dl>

 

 





