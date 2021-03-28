---
description: Se envía a un procedimiento DLL de extensión del administrador de archivos cuando el usuario presiona F1 en un elemento de comando de menú o barra de herramientas. La extensión debe llamar a WinHelp, con el parámetro HWND de la función establecido en el valor del parámetro HWND de la extensión.
title: Mensaje de FMEVENT_HELPMENUITEM (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: c20b5828a6e2362b9b9c13fc9b2986b0ea7b5fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984206"
---
# <a name="fmevent_helpmenuitem-message"></a><span data-ttu-id="91636-104">FMEVENT \_ HELPMENUITEM</span><span class="sxs-lookup"><span data-stu-id="91636-104">FMEVENT\_HELPMENUITEM message</span></span>

<span data-ttu-id="91636-105">Se envía a un procedimiento DLL de extensión del administrador de archivos cuando el usuario presiona F1 en un elemento de comando de menú o barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="91636-105">Sent to a File Manager extension DLL procedure when the user presses F1 on a menu or toolbar command item.</span></span> <span data-ttu-id="91636-106">La extensión debe llamar a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), con el parámetro *hWnd* de la función establecido en el valor del parámetro *hWnd* de la extensión.</span><span class="sxs-lookup"><span data-stu-id="91636-106">The extension should call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), with that function's *hwnd* parameter set to the value of the extension's *hwnd* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="91636-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91636-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91636-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91636-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="91636-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="91636-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="91636-110">*uItem*</span><span class="sxs-lookup"><span data-stu-id="91636-110">*uItem*</span></span> 
</dt> <dd>

<span data-ttu-id="91636-111">Valor que identifica el elemento de comando de menú o de la barra de herramientas para el que se desea obtener ayuda.</span><span class="sxs-lookup"><span data-stu-id="91636-111">A value that identifies the menu or toolbar command item for which Help is desired.</span></span> <span data-ttu-id="91636-112">El procedimiento de extensión usa este valor para determinar el mejor modo de llamar a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).</span><span class="sxs-lookup"><span data-stu-id="91636-112">The extension procedure uses this value to determine how best to call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91636-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91636-113">Return value</span></span>

<span data-ttu-id="91636-114">Un procedimiento de archivo DLL de extensión debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="91636-114">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="91636-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91636-115">Requirements</span></span>



| <span data-ttu-id="91636-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="91636-116">Requirement</span></span> | <span data-ttu-id="91636-117">Value</span><span class="sxs-lookup"><span data-stu-id="91636-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91636-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91636-118">Minimum supported client</span></span><br/> | <span data-ttu-id="91636-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="91636-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="91636-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91636-120">Minimum supported server</span></span><br/> | <span data-ttu-id="91636-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="91636-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="91636-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91636-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="91636-123"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="91636-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91636-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="91636-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91636-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="91636-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="91636-126">**FMEVENT \_ HELPSTRING**</span><span class="sxs-lookup"><span data-stu-id="91636-126">**FMEVENT\_HELPSTRING**</span></span>](fmevent-helpstring.md)
</dt> </dl>

 

 




