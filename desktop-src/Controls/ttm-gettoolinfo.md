---
title: Mensaje de TTM_GETTOOLINFO (commctrl. h)
description: Recupera la información que un control ToolTip mantiene sobre una herramienta.
ms.assetid: b94d3b78-2437-4c60-ba46-b3f57cf9c876
keywords:
- TTM_GETTOOLINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_GETTOOLINFO
- TTM_GETTOOLINFOA
- TTM_GETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc0de37b97be3bec495c8777b2ddd1cc6fc1bd42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150303"
---
# <a name="ttm_gettoolinfo-message"></a><span data-ttu-id="672f0-104">TTM \_ GETTOOLINFO</span><span class="sxs-lookup"><span data-stu-id="672f0-104">TTM\_GETTOOLINFO message</span></span>

<span data-ttu-id="672f0-105">Recupera la información que un control ToolTip mantiene sobre una herramienta.</span><span class="sxs-lookup"><span data-stu-id="672f0-105">Retrieves the information that a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="672f0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="672f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="672f0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="672f0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="672f0-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="672f0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="672f0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="672f0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="672f0-110">Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="672f0-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="672f0-111">Al enviar el mensaje, los miembros **hWnd** y **uId** identifican una herramienta y el miembro **cbSize** debe especificar el tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="672f0-111">When sending the message, the **hwnd** and **uId** members identify a tool, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="672f0-112">Al usar este mensaje para recuperar el texto de información sobre herramientas, asegúrese de que el miembro **lpszText** de la estructura **TOOLINFO** apunta a un búfer válido de tamaño de adquate</span><span class="sxs-lookup"><span data-stu-id="672f0-112">When using this message to retrieve the tooltip text, ensure that the **lpszText** member of the **TOOLINFO** structure points to a valid buffer of adquate size</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="672f0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="672f0-113">Return value</span></span>

<span data-ttu-id="672f0-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="672f0-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="672f0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="672f0-115">Remarks</span></span>

<span data-ttu-id="672f0-116">Si el control ToolTip incluye la herramienta, la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) recibe información sobre la herramienta.</span><span class="sxs-lookup"><span data-stu-id="672f0-116">If the tooltip control includes the tool, the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure receives information about the tool.</span></span>

## <a name="examples"></a><span data-ttu-id="672f0-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="672f0-117">Examples</span></span>

<span data-ttu-id="672f0-118">En el ejemplo siguiente se cambia la posición de un control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="672f0-118">The following example repositions a tooltip control.</span></span>


```C++
HRESULT MyToolTipClass::OffsetTooltip(int xOffset, int yOffset)  
{  
    HRESULT hr = S_OK;   
    DWORD   dwError = 0;  
  
    if (NULL != m_hWndToolTip)  
    {  
        TOOLINFO ti = {0};  
  
        ti.cbSize = sizeof(TOOLINFO);  
        ti.hwnd   = m_hWndToolTipOwner;  
  
        // Get the current tooltip definition.          
        if( SendMessage(m_hWndToolTip, TTM_GETTOOLINFO, 0, (LPARAM)&ti))  
        {  
            // Offset the tooltip rectangle as specified.              
            OffsetRect(&ti.rect, xOffset, yOffset);  
  
            // Apply the new rectangle to the tooltip.
            SendMessage(m_hWndToolTip, TTM_NEWTOOLRECT, 0, (LPARAM)&ti);  
        }  
        else  
        {  
            dwError = GetLastError();  
            hr = HRESULT_FROM_WIN32(dwError);  
            MyErrorHandler(hr);
       }  
    }  
    return hr;  
}  
```



## <a name="requirements"></a><span data-ttu-id="672f0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="672f0-119">Requirements</span></span>



| <span data-ttu-id="672f0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="672f0-120">Requirement</span></span> | <span data-ttu-id="672f0-121">Value</span><span class="sxs-lookup"><span data-stu-id="672f0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="672f0-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="672f0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="672f0-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="672f0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="672f0-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="672f0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="672f0-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="672f0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="672f0-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="672f0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="672f0-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="672f0-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="672f0-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="672f0-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="672f0-129">**TTM \_ GETTOOLINFOW** (Unicode) y **TTM \_ GETTOOLINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="672f0-129">**TTM\_GETTOOLINFOW** (Unicode) and **TTM\_GETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 





