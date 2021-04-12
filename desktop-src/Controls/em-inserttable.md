---
title: Mensaje EM_INSERTTABLE (RichEdit. h)
description: Inserta una o varias filas de tabla idénticas con celdas vacías.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- EM_INSERTTABLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_INSERTTABLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea5de278df98e412f219d246164221cfea75255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489448"
---
# <a name="em_inserttable-message"></a><span data-ttu-id="de8d5-104">\_Mensaje INSERTTABLE em</span><span class="sxs-lookup"><span data-stu-id="de8d5-104">EM\_INSERTTABLE message</span></span>

<span data-ttu-id="de8d5-105">Inserta una o varias filas de tabla idénticas con celdas vacías.</span><span class="sxs-lookup"><span data-stu-id="de8d5-105">Inserts one or more identical table rows with empty cells.</span></span>


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
```



## <a name="parameters"></a><span data-ttu-id="de8d5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de8d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de8d5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de8d5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de8d5-108">Puntero a una estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="de8d5-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="de8d5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de8d5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de8d5-110">Puntero a una estructura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="de8d5-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de8d5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de8d5-111">Return value</span></span>

<span data-ttu-id="de8d5-112">Devuelve S \_ OK si se inserta la tabla o un código de error si no lo está.</span><span class="sxs-lookup"><span data-stu-id="de8d5-112">Returns S\_OK if the table is inserted, or an error code if not.</span></span>

## <a name="remarks"></a><span data-ttu-id="de8d5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de8d5-113">Remarks</span></span>

<span data-ttu-id="de8d5-114">Si el miembro **cpStartRow** de [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) es 1, este mensaje elimina el texto seleccionado (si existe) y, a continuación, inserta filas de tabla vacías con los parámetros de fila y celda proporcionados por *wParam* e *lParam*.</span><span class="sxs-lookup"><span data-stu-id="de8d5-114">If the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) is  1, this message deletes the selected text (if any), and then inserts empty table rows with the row and cell parameters given by *wParam* and *lParam*.</span></span> <span data-ttu-id="de8d5-115">Deja la selección que apunta al principio de la primera celda de la primera fila.</span><span class="sxs-lookup"><span data-stu-id="de8d5-115">It leaves the selection pointing to the start of the first cell in the first row.</span></span> <span data-ttu-id="de8d5-116">A continuación, el cliente puede rellenar las celdas de la tabla seleccionando la selección (o un [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) a las distintas marcas de final de celda e insertando y dando formato al texto deseado.</span><span class="sxs-lookup"><span data-stu-id="de8d5-116">The client can then populate the table cells by pointing the selection (or an [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) to the various cell end marks and inserting and formatting the desired text.</span></span> <span data-ttu-id="de8d5-117">Dicho texto puede incluir filas de tabla anidada.</span><span class="sxs-lookup"><span data-stu-id="de8d5-117">Such text can include nested table rows.</span></span> <span data-ttu-id="de8d5-118">Como alternativa, si el miembro **cpStartRow** de **TABLEROWPARMS** es 0 o superior, las filas de la tabla se insertan en la posición de carácter proporcionada por **cpStartRow**.</span><span class="sxs-lookup"><span data-stu-id="de8d5-118">Alternatively, if the **cpStartRow** member of the **TABLEROWPARMS** is 0 or greater, table rows are inserted at the character position given by **cpStartRow**.</span></span> <span data-ttu-id="de8d5-119">Esto solo cambia la selección actual si la tabla se inserta dentro del texto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="de8d5-119">This only changes the current selection if the table is inserted inside the selected text.</span></span>

<span data-ttu-id="de8d5-120">Una tabla de edición enriquecida de Microsoft está formada por una secuencia de filas de la tabla que, a su vez, constan de secuencias de párrafos.</span><span class="sxs-lookup"><span data-stu-id="de8d5-120">A Microsoft Rich Edit table consists of a sequence of table rows which, in turn, consist of sequences of paragraphs.</span></span> <span data-ttu-id="de8d5-121">Una fila de tabla comienza con el párrafo especial de delimitador de dos caracteres U + FFF9 U + 000D y termina con el párrafo de delimitador de dos caracteres U + FFFB U + 000D.</span><span class="sxs-lookup"><span data-stu-id="de8d5-121">A table row starts with the special two-character delimiter paragraph U+FFF9 U+000D and ends with the two-character delimiter paragraph U+FFFB U+000D.</span></span> <span data-ttu-id="de8d5-122">Cada celda se termina con la marca de celda U + 0007, que se trata como una marca de final de párrafo de forma rígida como U + 000D (CR).</span><span class="sxs-lookup"><span data-stu-id="de8d5-122">Each cell is terminated by the cell mark U+0007, which is treated as a hard end-of-paragraph mark just as U+000D (CR) is.</span></span> <span data-ttu-id="de8d5-123">Los parámetros de celda y fila de la tabla se tratan como un formato de párrafo especial de los delimitadores de fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="de8d5-123">The table row and cell parameters are treated as special paragraph formatting of the table-row delimiters.</span></span> <span data-ttu-id="de8d5-124">El formato contiene la información de la estructura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="de8d5-124">The formatting contains the information in the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span> <span data-ttu-id="de8d5-125">Los parámetros de celda proporcionados por la estructura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) se almacenan en una versión expandida de la matriz Tabs.</span><span class="sxs-lookup"><span data-stu-id="de8d5-125">The cell parameters given by the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure are stored in an expanded version of the tabs array.</span></span> <span data-ttu-id="de8d5-126">Este formato permite anidar tablas dentro de otras tablas, hasta quince niveles de profundidad.</span><span class="sxs-lookup"><span data-stu-id="de8d5-126">This format allows tables to be nested within other tables, up to fifteen levels deep.</span></span>

## <a name="requirements"></a><span data-ttu-id="de8d5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de8d5-127">Requirements</span></span>



| <span data-ttu-id="de8d5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="de8d5-128">Requirement</span></span> | <span data-ttu-id="de8d5-129">Value</span><span class="sxs-lookup"><span data-stu-id="de8d5-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de8d5-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de8d5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="de8d5-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="de8d5-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="de8d5-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de8d5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="de8d5-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="de8d5-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de8d5-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de8d5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="de8d5-135"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="de8d5-135"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de8d5-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="de8d5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de8d5-137">**\_INSERTIMAGE em**</span><span class="sxs-lookup"><span data-stu-id="de8d5-137">**EM\_INSERTIMAGE**</span></span>](em-insertimage.md)
</dt> </dl>

 

 





