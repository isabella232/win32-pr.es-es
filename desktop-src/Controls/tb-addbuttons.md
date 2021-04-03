---
title: Mensaje de TB_ADDBUTTONS (commctrl. h)
description: Agrega uno o más botones a una barra de herramientas.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- TB_ADDBUTTONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_ADDBUTTONS
- TB_ADDBUTTONSA
- TB_ADDBUTTONSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f954e9a133f78a9415358d1c7f61d68008cd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997178"
---
# <a name="tb_addbuttons-message"></a><span data-ttu-id="f685b-104">\_Mensaje ADDBUTTONS TB</span><span class="sxs-lookup"><span data-stu-id="f685b-104">TB\_ADDBUTTONS message</span></span>

<span data-ttu-id="f685b-105">Agrega uno o más botones a una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f685b-105">Adds one or more buttons to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f685b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f685b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f685b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f685b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f685b-108">Número de botones que se van a agregar.</span><span class="sxs-lookup"><span data-stu-id="f685b-108">Number of buttons to add.</span></span>

</dd> <dt>

<span data-ttu-id="f685b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f685b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f685b-110">Puntero a una matriz de estructuras [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que contienen información sobre los botones que se van a agregar.</span><span class="sxs-lookup"><span data-stu-id="f685b-110">Pointer to an array of [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures that contain information about the buttons to add.</span></span> <span data-ttu-id="f685b-111">Debe haber el mismo número de elementos en la matriz que los botones especificados por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="f685b-111">There must be the same number of elements in the array as buttons specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f685b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f685b-112">Return value</span></span>

<span data-ttu-id="f685b-113">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f685b-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f685b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f685b-114">Remarks</span></span>

<span data-ttu-id="f685b-115">Si la barra de herramientas se creó mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , debe enviar el mensaje de [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) a la barra de herramientas antes de enviar **TB \_ ADDBUTTONS**.</span><span class="sxs-lookup"><span data-stu-id="f685b-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBUTTONS**.</span></span>

<span data-ttu-id="f685b-116">Vea [**TB \_ SETIMAGELIST**](tb-setimagelist.md) para obtener una explicación de cómo asignar mapas de bits a los botones de la barra de herramientas de una o varias listas de imágenes.</span><span class="sxs-lookup"><span data-stu-id="f685b-116">See [**TB\_SETIMAGELIST**](tb-setimagelist.md) for a discussion of how to assign bitmaps to toolbar buttons from one or more image lists.</span></span>

## <a name="examples"></a><span data-ttu-id="f685b-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f685b-117">Examples</span></span>

<span data-ttu-id="f685b-118">En el ejemplo de código siguiente se agregan tres botones a una barra de herramientas, utilizando el mapa de bits estándar del sistema para botones de vista.</span><span class="sxs-lookup"><span data-stu-id="f685b-118">The following example code adds three buttons to a toolbar, using the standard system bitmap for view buttons.</span></span> <span data-ttu-id="f685b-119">El mensaje [**TB \_ ADDBITMAP**](tb-addbitmap.md) devuelve el índice de la primera imagen de botón en la lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="f685b-119">The [**TB\_ADDBITMAP**](tb-addbitmap.md) message returns the index of the first button image within the image list.</span></span> <span data-ttu-id="f685b-120">Las imágenes individuales se identifican por sus desplazamientos a partir de ese valor.</span><span class="sxs-lookup"><span data-stu-id="f685b-120">Individual images are identified by their offsets from that value.</span></span>


```C++
TBADDBITMAP tbAddBitmap;
tbAddBitmap.hInst = HINST_COMMCTRL;
tbAddBitmap.nID = IDB_VIEW_SMALL_COLOR;

// There are 12 items in IDB_VIEW_SMALL_COLOR.  However, because this is a standard
// system-defined bitmap, the wParam (nButtons) is ignored.
//
// hWndToolbar is the handle of the toolbar window.
//
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was created
// by using CreateWindowEx.
//
int stdidx = SendMessage(hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tbAddBitmap);

// Define the buttons. 
// IDM_SETLARGEICONVIEW and so on are application-defined command IDs.

const int numButtons = 3;
TBBUTTON tbButtonsAdd[numButtons] = 
{
    {stdidx + VIEW_LARGEICONS, IDM_SETLARGEICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_SMALLICONS, IDM_SETSMALLICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_DETAILS, IDM_SETDETAILSVIEW, TBSTATE_ENABLED, BTNS_BUTTON}
}; 

// Add the view buttons.
SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)tbButtonsAdd);
```



## <a name="requirements"></a><span data-ttu-id="f685b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f685b-121">Requirements</span></span>



| <span data-ttu-id="f685b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f685b-122">Requirement</span></span> | <span data-ttu-id="f685b-123">Value</span><span class="sxs-lookup"><span data-stu-id="f685b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f685b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f685b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f685b-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f685b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f685b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f685b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f685b-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f685b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f685b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f685b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f685b-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f685b-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f685b-130">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f685b-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f685b-131">**TB \_ ADDBUTTONSW** (Unicode) y **TB \_ ADDBUTTONSA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f685b-131">**TB\_ADDBUTTONSW** (Unicode) and **TB\_ADDBUTTONSA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f685b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f685b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f685b-133">**Valores de índice de imagen de botón estándar de la barra de herramientas**</span><span class="sxs-lookup"><span data-stu-id="f685b-133">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

