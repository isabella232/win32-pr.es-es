---
title: Mensaje de TTM_ADJUSTRECT (commctrl. h)
description: Calcula el rectángulo de presentación del texto de un control ToolTip desde su rectángulo de ventana o el rectángulo de la ventana de información sobre herramientas necesario para mostrar un rectángulo de presentación de texto especificado.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- TTM_ADJUSTRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af89374161d5e3f9d9ab6affc2b3b498a39cbf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996416"
---
# <a name="ttm_adjustrect-message"></a><span data-ttu-id="69267-104">TTM \_ ADJUSTRECT</span><span class="sxs-lookup"><span data-stu-id="69267-104">TTM\_ADJUSTRECT message</span></span>

<span data-ttu-id="69267-105">Calcula el rectángulo de presentación del texto de un control ToolTip desde su rectángulo de ventana o el rectángulo de la ventana de información sobre herramientas necesario para mostrar un rectángulo de presentación de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="69267-105">Calculates a tooltip control's text display rectangle from its window rectangle, or the tooltip window rectangle needed to display a specified text display rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="69267-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69267-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69267-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69267-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69267-108">Valor que especifica la operación que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="69267-108">Value that specifies which operation to perform.</span></span> <span data-ttu-id="69267-109">Si es **true**, *lParam* se usa para especificar un rectángulo de presentación de texto y recibe el rectángulo de ventana correspondiente.</span><span class="sxs-lookup"><span data-stu-id="69267-109">If **TRUE**, *lParam* is used to specify a text-display rectangle and it receives the corresponding window rectangle.</span></span> <span data-ttu-id="69267-110">Si es **false**, *lParam* se usa para especificar un rectángulo de ventana y recibe el rectángulo de presentación de texto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="69267-110">If **FALSE**, *lParam* is used to specify a window rectangle and it receives the corresponding text display rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="69267-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69267-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69267-112">Estructura **Rect** para contener un rectángulo de la ventana de información sobre herramientas o un rectángulo de presentación de texto.</span><span class="sxs-lookup"><span data-stu-id="69267-112">**RECT** structure to hold either a tooltip window rectangle or a text display rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69267-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69267-113">Return value</span></span>

<span data-ttu-id="69267-114">Devuelve un valor distinto de cero si el rectángulo se ajusta correctamente y devuelve cero si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="69267-114">Returns a nonzero value if the rectangle is successfully adjusted, and returns zero if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="69267-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69267-115">Remarks</span></span>

<span data-ttu-id="69267-116">Este mensaje es especialmente útil si desea utilizar un control de información sobre herramientas para mostrar el texto completo de una cadena que se suele truncar.</span><span class="sxs-lookup"><span data-stu-id="69267-116">This message is particularly useful when you want to use a tooltip control to display the full text of a string that is usually truncated.</span></span> <span data-ttu-id="69267-117">Se suele usar con los controles ListView y TreeView.</span><span class="sxs-lookup"><span data-stu-id="69267-117">It is commonly used with listview and treeview controls.</span></span> <span data-ttu-id="69267-118">Normalmente envía este mensaje en respuesta a un [TTN \_ Mostrar](ttn-show.md) código de notificación para que pueda colocar el control de información sobre herramientas correctamente.</span><span class="sxs-lookup"><span data-stu-id="69267-118">You typically send this message in response to a [TTN\_SHOW](ttn-show.md) notification code so that you can position the tooltip control properly.</span></span>

<span data-ttu-id="69267-119">El rectángulo de la ventana de información sobre herramientas es algo más grande que el rectángulo de presentación de texto que delimita la cadena de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="69267-119">The tooltip window rectangle is somewhat larger than the text display rectangle that bounds the tooltip string.</span></span> <span data-ttu-id="69267-120">El origen de la ventana también está desplazado hacia arriba y a la izquierda desde el origen del rectángulo de presentación del texto.</span><span class="sxs-lookup"><span data-stu-id="69267-120">The window origin is also offset up and to the left from the origin of the text display rectangle.</span></span> <span data-ttu-id="69267-121">Para colocar el rectángulo de presentación de texto, debe calcular el rectángulo de ventana correspondiente y usar ese rectángulo para colocar la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="69267-121">To position the text display rectangle, you must calculate the corresponding window rectangle and use that rectangle to position the tooltip.</span></span> <span data-ttu-id="69267-122">**TTM \_ ADJUSTRECT** controla este cálculo.</span><span class="sxs-lookup"><span data-stu-id="69267-122">**TTM\_ADJUSTRECT** handles this calculation for you.</span></span>

<span data-ttu-id="69267-123">Si establece *wParam* en **true**, **TTM \_ ADJUSTRECT** toma el tamaño y la posición del rectángulo de visualización del texto de información sobre herramientas deseado y devuelve el tamaño y la posición de la ventana de información sobre herramientas necesaria para mostrar el texto en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="69267-123">If you set *wParam* to **TRUE**, **TTM\_ADJUSTRECT** takes the size and position of the desired tooltip text display rectangle, and passes back the size and position of the tooltip window needed to display the text in the specified position.</span></span> <span data-ttu-id="69267-124">Si establece *wParam* en **false**, puede especificar un rectángulo de la ventana de información sobre herramientas y **TTM \_ ADJUSTRECT** devolverá el tamaño y la posición de su rectángulo de texto.</span><span class="sxs-lookup"><span data-stu-id="69267-124">If you set *wParam* to **FALSE**, you can specify a tooltip window rectangle and **TTM\_ADJUSTRECT** will return the size and position of its text rectangle.</span></span>

<span data-ttu-id="69267-125">En el fragmento de código siguiente se muestra el uso del mensaje **TTM \_ ADJUSTRECT** para colocar un control ToolTip para que muestre el texto completo de la cadena de un control en lugar de una cadena truncada.</span><span class="sxs-lookup"><span data-stu-id="69267-125">The following code fragment illustrates the use of the **TTM\_ADJUSTRECT** message to position a tooltip control to display the full text of a control's string in place of a truncated string.</span></span> <span data-ttu-id="69267-126">La función **GetMyItemRect** definida por la aplicación devuelve el rectángulo de texto que será necesario para mostrar el texto de información sobre herramientas directamente sobre la cadena truncada.</span><span class="sxs-lookup"><span data-stu-id="69267-126">The application-defined **GetMyItemRect** function returns the text rectangle that will be needed to display the tooltip text directly over the truncated string.</span></span> <span data-ttu-id="69267-127">Los detalles de cómo se implementa esta función dependerán del control determinado.</span><span class="sxs-lookup"><span data-stu-id="69267-127">The details of how this function is implemented will depend on the particular control.</span></span> <span data-ttu-id="69267-128">**TTM \_ ADJUSTRECT** se usa para enviar este rectángulo de texto al control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="69267-128">**TTM\_ADJUSTRECT** is used to send this text rectangle to the tooltip control.</span></span> <span data-ttu-id="69267-129">Devuelve un rectángulo de ventana colocado y con el tamaño adecuado que se usa para colocar la ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="69267-129">It returns an appropriately sized and positioned window rectangle that is then used to position the tooltip window.</span></span>


```
case TTN_SHOW:

if (MyStringIsTruncated) {
    RECT rc;
    
    GetMyItemRect(&rc);
    SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
    SetWindowPos(hwndToolTip,
                 NULL,
                 rc.left, rc.top,
                 0, 0,
                 SWP_NOSIZE|SWP_NOZORDER|SWP_NOACTIVATE);
} 
```



## <a name="requirements"></a><span data-ttu-id="69267-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69267-130">Requirements</span></span>



| <span data-ttu-id="69267-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="69267-131">Requirement</span></span> | <span data-ttu-id="69267-132">Value</span><span class="sxs-lookup"><span data-stu-id="69267-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69267-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69267-133">Minimum supported client</span></span><br/> | <span data-ttu-id="69267-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="69267-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69267-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69267-135">Minimum supported server</span></span><br/> | <span data-ttu-id="69267-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="69267-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69267-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69267-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="69267-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="69267-138"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





