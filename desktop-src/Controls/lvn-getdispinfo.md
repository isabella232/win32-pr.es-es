---
title: Código de notificación de LVN_GETDISPINFO (commctrl. h)
description: Enviado por un control de vista de lista a su ventana primaria. Es una solicitud para que la ventana primaria proporcione la información necesaria para mostrar u ordenar un elemento de vista de lista. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- LVN_GETDISPINFO controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804153"
---
# <a name="lvn_getdispinfo-notification-code"></a><span data-ttu-id="d5be0-106">Código de notificación de GETDISPINFO de LVN \_</span><span class="sxs-lookup"><span data-stu-id="d5be0-106">LVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="d5be0-107">Enviado por un control de vista de lista a su ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="d5be0-107">Sent by a list-view control to its parent window.</span></span> <span data-ttu-id="d5be0-108">Es una solicitud para que la ventana primaria proporcione la información necesaria para mostrar u ordenar un elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="d5be0-108">It is a request for the parent window to provide information needed to display or sort a list-view item.</span></span> <span data-ttu-id="d5be0-109">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d5be0-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="d5be0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5be0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5be0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5be0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5be0-112">Puntero a una estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="d5be0-112">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="d5be0-113">En la entrada, la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) contenida en esta estructura especifica el tipo de información requerida e identifica el elemento o subelemento de interés.</span><span class="sxs-lookup"><span data-stu-id="d5be0-113">On input, the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure contained in this structure specifies the type of information required and identifies the item or subitem of interest.</span></span> <span data-ttu-id="d5be0-114">Use la estructura **LVITEM** para devolver la información solicitada al control.</span><span class="sxs-lookup"><span data-stu-id="d5be0-114">Use the **LVITEM** structure to return the requested information to the control.</span></span> <span data-ttu-id="d5be0-115">Si el controlador de mensajes establece la \_ marca LVIF di \_ SETITEM en el miembro **Mask** de la estructura **LVITEM** , el control de vista de lista almacena la información solicitada y no la pedirá de nuevo.</span><span class="sxs-lookup"><span data-stu-id="d5be0-115">If your message handler sets the LVIF\_DI\_SETITEM flag in the **mask** member of the **LVITEM** structure, the list-view control stores the requested information and will not ask for it again.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5be0-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5be0-116">Return value</span></span>

<span data-ttu-id="d5be0-117">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d5be0-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5be0-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5be0-118">Remarks</span></span>

<span data-ttu-id="d5be0-119">El receptor de notificaciones convierte *lParam* para recuperar la estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="d5be0-119">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="d5be0-120">El parámetro *wParam* contiene el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="d5be0-120">The *wParam* parameter contains the notification code.</span></span>

<span data-ttu-id="d5be0-121">Un control de vista de lista envía el código de notificación **LVN \_ GETDISPINFO** para recuperar la información de los elementos que almacena la aplicación en lugar del control.</span><span class="sxs-lookup"><span data-stu-id="d5be0-121">A list-view control sends the **LVN\_GETDISPINFO** notification code to retrieve item information that is stored by the application rather than the control.</span></span> <span data-ttu-id="d5be0-122">La información puede ser información de texto o de icono para un elemento.</span><span class="sxs-lookup"><span data-stu-id="d5be0-122">The information can be text or icon information for an item.</span></span> <span data-ttu-id="d5be0-123">También puede ser información sobre el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="d5be0-123">It can also be item state information.</span></span> <span data-ttu-id="d5be0-124">Vea el mensaje [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) para obtener más información sobre cómo implementar el estado del elemento en una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="d5be0-124">See the [**LVM\_SETCALLBACKMASK**](lvm-setcallbackmask.md) message for more information on implementing item state on a callback basis.</span></span>

<span data-ttu-id="d5be0-125">Para obtener más información sobre las devoluciones de llamada de vista de lista, vea [elementos de devolución de llamada y máscara de devolución de llamada](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d5be0-125">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d5be0-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d5be0-126">Examples</span></span>

<span data-ttu-id="d5be0-127">En el ejemplo siguiente se muestra cómo se puede controlar este código de notificación para establecer el texto de las columnas de una vista de lista.</span><span class="sxs-lookup"><span data-stu-id="d5be0-127">The following example shows how this notification code might be handled to set the text in the columns of a list view.</span></span> <span data-ttu-id="d5be0-128">Los datos de cada elemento se guardan en la estructura siguiente.</span><span class="sxs-lookup"><span data-stu-id="d5be0-128">The data for each item is held in the following structure.</span></span>


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



<span data-ttu-id="d5be0-129">A continuación se indica el \_ controlador de notificaciones de WM en el procedimiento de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d5be0-129">The following is from the WM\_NOTIFY handler in the dialog procedure.</span></span>


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a><span data-ttu-id="d5be0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5be0-130">Requirements</span></span>



| <span data-ttu-id="d5be0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5be0-131">Requirement</span></span> | <span data-ttu-id="d5be0-132">Value</span><span class="sxs-lookup"><span data-stu-id="d5be0-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5be0-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5be0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d5be0-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d5be0-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5be0-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5be0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d5be0-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5be0-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5be0-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5be0-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5be0-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5be0-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d5be0-139">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="d5be0-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d5be0-140">**LVN \_ GETDISPINFOW** (Unicode) y **LVN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d5be0-140">**LVN\_GETDISPINFOW** (Unicode) and **LVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="d5be0-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5be0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5be0-142">**LVN \_ SETDISPINFO**</span><span class="sxs-lookup"><span data-stu-id="d5be0-142">**LVN\_SETDISPINFO**</span></span>](lvn-setdispinfo.md)
</dt> </dl>

 

 





