---
description: La función IsWindowRedirectedForPrint determina si la ventana especificada se redirige actualmente para imprimirla.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: IsWindowRedirectedForPrint función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720728"
---
# <a name="iswindowredirectedforprint-function"></a><span data-ttu-id="17ad0-103">IsWindowRedirectedForPrint función)</span><span class="sxs-lookup"><span data-stu-id="17ad0-103">IsWindowRedirectedForPrint function</span></span>

<span data-ttu-id="17ad0-104">La función **IsWindowRedirectedForPrint** determina si la ventana especificada se redirige actualmente para imprimirla.</span><span class="sxs-lookup"><span data-stu-id="17ad0-104">The **IsWindowRedirectedForPrint** function determines whether the specified window is currently redirected for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="17ad0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17ad0-105">Syntax</span></span>


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="17ad0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17ad0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17ad0-107">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17ad0-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17ad0-108">Controlador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="17ad0-108">The handle of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17ad0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17ad0-109">Return value</span></span>

<span data-ttu-id="17ad0-110">Si la ventana se redirige actualmente para imprimirla, la función devuelve un valor distinto de cero; de lo contrario, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="17ad0-110">If the window is currently redirected for printing, the function returns a nonzero value; otherwise, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="17ad0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17ad0-111">Remarks</span></span>

<span data-ttu-id="17ad0-112">Una ventana se redirige para imprimir cuando procesa una llamada a [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow).</span><span class="sxs-lookup"><span data-stu-id="17ad0-112">A window is redirected for printing when it processes a call to [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow).</span></span> <span data-ttu-id="17ad0-113">En una llamada a **PrintWindow**, una ventana representa su contenido en un contexto de dispositivo fuera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="17ad0-113">In a call to **PrintWindow**, a window renders its content to an off-screen device context.</span></span>

<span data-ttu-id="17ad0-114">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="17ad0-114">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="17ad0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17ad0-115">Requirements</span></span>



| <span data-ttu-id="17ad0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="17ad0-116">Requirement</span></span> | <span data-ttu-id="17ad0-117">Value</span><span class="sxs-lookup"><span data-stu-id="17ad0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17ad0-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17ad0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="17ad0-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="17ad0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17ad0-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17ad0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="17ad0-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="17ad0-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17ad0-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17ad0-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17ad0-123"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17ad0-123"><dt>User32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17ad0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="17ad0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17ad0-125">**PrintWindow**</span><span class="sxs-lookup"><span data-stu-id="17ad0-125">**PrintWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[<span data-ttu-id="17ad0-126">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="17ad0-126">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="17ad0-127">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="17ad0-127">**LoadLibrary**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="17ad0-128">**impresión de WM \_**</span><span class="sxs-lookup"><span data-stu-id="17ad0-128">**WM\_PRINT**</span></span>](/windows/desktop/gdi/wm-print)
</dt> <dt>

[<span data-ttu-id="17ad0-129">**PRINTCLIENT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="17ad0-129">**WM\_PRINTCLIENT**</span></span>](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

