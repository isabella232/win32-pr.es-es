---
title: HWINEVENTHOOK (WINDEF. h)
description: Se usa para declarar una función de enlace de eventos de ventana.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695942"
---
# <a name="hwineventhook"></a><span data-ttu-id="269da-104">HWINEVENTHOOK</span><span class="sxs-lookup"><span data-stu-id="269da-104">HWINEVENTHOOK</span></span>

<span data-ttu-id="269da-105">Se usa para declarar una función de enlace de eventos de ventana.</span><span class="sxs-lookup"><span data-stu-id="269da-105">Used to declare a window event hook function.</span></span>


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a><span data-ttu-id="269da-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="269da-106">Remarks</span></span>

<span data-ttu-id="269da-107">Este tipo de datos se usa con la función de devolución de llamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) y las funciones [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) y [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) .</span><span class="sxs-lookup"><span data-stu-id="269da-107">This data type is used with the [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function and the [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="269da-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="269da-108">Requirements</span></span>



| <span data-ttu-id="269da-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="269da-109">Requirement</span></span> | <span data-ttu-id="269da-110">Value</span><span class="sxs-lookup"><span data-stu-id="269da-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="269da-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="269da-111">Minimum supported client</span></span><br/> | <span data-ttu-id="269da-112">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="269da-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="269da-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="269da-113">Minimum supported server</span></span><br/> | <span data-ttu-id="269da-114">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="269da-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                          |
| <span data-ttu-id="269da-115">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="269da-115">Redistributable</span></span><br/>          | <span data-ttu-id="269da-116">Active Accessibility 1,3 RDK en Windows NT 4,0 con SP6 y versiones posteriores y Windows 95</span><span class="sxs-lookup"><span data-stu-id="269da-116">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>                                   |
| <span data-ttu-id="269da-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="269da-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="269da-118"><dt>WINDEF. h (WINVER >= 0x0500) (incluye Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="269da-118"><dt>Windef.h (WINVER >= 0x0500) (include Windows.h)</dt></span></span> </dl> |



 

 





