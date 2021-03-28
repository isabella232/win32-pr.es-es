---
description: Una aplicación envía el mensaje de FONTCHANGE de WM \_ a todas las ventanas de nivel superior del sistema después de cambiar el grupo de recursos de fuente.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: Mensaje de WM_FONTCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b40650f0077ed854b87a6fd10e1dae610f0c3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985803"
---
# <a name="wm_fontchange-message"></a><span data-ttu-id="4fca6-103">Mensaje de FONTCHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="4fca6-103">WM\_FONTCHANGE message</span></span>

<span data-ttu-id="4fca6-104">Una aplicación envía el mensaje de **\_ FONTCHANGE de WM** a todas las ventanas de nivel superior del sistema después de cambiar el grupo de recursos de fuente.</span><span class="sxs-lookup"><span data-stu-id="4fca6-104">An application sends the **WM\_FONTCHANGE** message to all top-level windows in the system after changing the pool of font resources.</span></span>

<span data-ttu-id="4fca6-105">Para enviar este mensaje, llame a la función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="4fca6-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="4fca6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fca6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fca6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4fca6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fca6-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4fca6-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4fca6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4fca6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fca6-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4fca6-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fca6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fca6-111">Remarks</span></span>

<span data-ttu-id="4fca6-112">Una aplicación que agrega o quita fuentes del sistema (por ejemplo, mediante la función [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) o [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) ) debe enviar este mensaje a todas las ventanas de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="4fca6-112">An application that adds or removes fonts from the system (for example, by using the [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) or [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) function) should send this message to all top-level windows.</span></span>

<span data-ttu-id="4fca6-113">Para enviar el mensaje de **\_ FONTCHANGE de WM** a todas las ventanas de nivel superior, una aplicación puede llamar a la función **SendMessage** con el parámetro *hWnd* establecido en la \_ difusión HWND.</span><span class="sxs-lookup"><span data-stu-id="4fca6-113">To send the **WM\_FONTCHANGE** message to all top-level windows, an application can call the **SendMessage** function with the *hwnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fca6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fca6-114">Requirements</span></span>



| <span data-ttu-id="4fca6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fca6-115">Requirement</span></span> | <span data-ttu-id="4fca6-116">Value</span><span class="sxs-lookup"><span data-stu-id="4fca6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fca6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fca6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4fca6-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4fca6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4fca6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fca6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4fca6-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4fca6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4fca6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fca6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fca6-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4fca6-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fca6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fca6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fca6-124">Información general sobre fuentes y texto</span><span class="sxs-lookup"><span data-stu-id="4fca6-124">Fonts and Text Overview</span></span>](fonts-and-text.md)
</dt> <dt>

[<span data-ttu-id="4fca6-125">Mensajes de texto y fuente</span><span class="sxs-lookup"><span data-stu-id="4fca6-125">Font and Text Messages</span></span>](font-and-text-messages.md)
</dt> <dt>

[<span data-ttu-id="4fca6-126">**AddFontResource**</span><span class="sxs-lookup"><span data-stu-id="4fca6-126">**AddFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[<span data-ttu-id="4fca6-127">**RemoveFontResource**</span><span class="sxs-lookup"><span data-stu-id="4fca6-127">**RemoveFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
