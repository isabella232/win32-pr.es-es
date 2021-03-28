---
description: Se envía cuando el usuario coloca un archivo en la ventana de una aplicación que se ha registrado como destinatario de archivos colocados.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: Mensaje de WM_DROPFILES (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985394"
---
# <a name="wm_dropfiles-message"></a><span data-ttu-id="011c2-103">Mensaje de DROPFILES de WM \_</span><span class="sxs-lookup"><span data-stu-id="011c2-103">WM\_DROPFILES message</span></span>

<span data-ttu-id="011c2-104">Se envía cuando el usuario coloca un archivo en la ventana de una aplicación que se ha registrado como destinatario de archivos colocados.</span><span class="sxs-lookup"><span data-stu-id="011c2-104">Sent when the user drops a file on the window of an application that has registered itself as a recipient of dropped files.</span></span>


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a><span data-ttu-id="011c2-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="011c2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="011c2-106">*hDrop*</span><span class="sxs-lookup"><span data-stu-id="011c2-106">*hDrop*</span></span> 
</dt> <dd>

<span data-ttu-id="011c2-107">Identificador de una estructura interna que describe los archivos colocados.</span><span class="sxs-lookup"><span data-stu-id="011c2-107">A handle to an internal structure describing the dropped files.</span></span> <span data-ttu-id="011c2-108">Pase este identificador [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)o [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) para recuperar información acerca de los archivos colocados.</span><span class="sxs-lookup"><span data-stu-id="011c2-108">Pass this handle [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea), or [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) to retrieve information about the dropped files.</span></span>

</dd> <dt>

<span data-ttu-id="011c2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="011c2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="011c2-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="011c2-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="011c2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="011c2-111">Return value</span></span>

<span data-ttu-id="011c2-112">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="011c2-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="011c2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="011c2-113">Remarks</span></span>

<span data-ttu-id="011c2-114">El identificador HDROP se declara en ShellAPI. h.</span><span class="sxs-lookup"><span data-stu-id="011c2-114">The HDROP handle is declared in Shellapi.h.</span></span> <span data-ttu-id="011c2-115">Debe incluir este encabezado en la compilación para usar **WM \_ DROPFILES**.</span><span class="sxs-lookup"><span data-stu-id="011c2-115">You must include this header in your build to use **WM\_DROPFILES**.</span></span> <span data-ttu-id="011c2-116">Para obtener más información sobre cómo usar arrastrar y colocar para transferir datos de Shell, consulte transferencia de [datos de Shell mediante arrastrar y colocar o el portapapeles](dragdrop.md).</span><span class="sxs-lookup"><span data-stu-id="011c2-116">For further discussion of how to use drag-and-drop to transfer Shell data, see [Transferring Shell Data Using Drag-and-Drop or the Clipboard](dragdrop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="011c2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="011c2-117">Requirements</span></span>



| <span data-ttu-id="011c2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="011c2-118">Requirement</span></span> | <span data-ttu-id="011c2-119">Value</span><span class="sxs-lookup"><span data-stu-id="011c2-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="011c2-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="011c2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="011c2-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="011c2-121">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="011c2-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="011c2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="011c2-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="011c2-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="011c2-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="011c2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="011c2-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="011c2-125"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="011c2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="011c2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="011c2-127">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="011c2-127">**PostMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="011c2-128">**DragAcceptFiles**</span><span class="sxs-lookup"><span data-stu-id="011c2-128">**DragAcceptFiles**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
