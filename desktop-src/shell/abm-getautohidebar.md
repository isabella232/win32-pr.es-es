---
description: Recupera el identificador del Appbar de ocultación automático asociado a un borde de la pantalla. Si el sistema tiene varios monitores, se utiliza el monitor que contiene la barra de tareas principal.
title: Mensaje de ABM_GETAUTOHIDEBAR (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 545dd1d9-8cbb-4ff3-b871-4908ecac56db
api_name:
- ABM_GETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 979825a9dbc28a89e3579419542877faacbace45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153927"
---
# <a name="abm_getautohidebar-message"></a><span data-ttu-id="313c0-104">ABN \_ GETAUTOHIDEBAR</span><span class="sxs-lookup"><span data-stu-id="313c0-104">ABM\_GETAUTOHIDEBAR message</span></span>

<span data-ttu-id="313c0-105">Recupera el identificador del Appbar de ocultación automático asociado a un borde de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="313c0-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="313c0-106">Si el sistema tiene varios monitores, se utiliza el monitor que contiene la barra de tareas principal.</span><span class="sxs-lookup"><span data-stu-id="313c0-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="313c0-107">Para consultar un Appbar de ocultación automáticamente en un monitor específico, use [**ABN \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md).</span><span class="sxs-lookup"><span data-stu-id="313c0-107">To query for an autohide appbar on a specific monitor, use [**ABM\_GETAUTOHIDEBAREX**](abm-getautohidebarex.md).</span></span>

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="313c0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="313c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="313c0-109">*pabd*</span><span class="sxs-lookup"><span data-stu-id="313c0-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="313c0-110">Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que especifica el borde de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="313c0-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge.</span></span> <span data-ttu-id="313c0-111">Debe especificar los miembros **cbSize** y **uEdge** al enviar este mensaje; se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="313c0-111">You must specify the **cbSize** and **uEdge** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="313c0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="313c0-112">Return value</span></span>

<span data-ttu-id="313c0-113">Devuelve el identificador del Appbar de ocultación automáticamente.</span><span class="sxs-lookup"><span data-stu-id="313c0-113">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="313c0-114">El valor devuelto es **null** si se produce un error o si no hay ningún Appbar de ocultación automático asociado al borde especificado.</span><span class="sxs-lookup"><span data-stu-id="313c0-114">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge.</span></span>

## <a name="requirements"></a><span data-ttu-id="313c0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="313c0-115">Requirements</span></span>



| <span data-ttu-id="313c0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="313c0-116">Requirement</span></span> | <span data-ttu-id="313c0-117">Value</span><span class="sxs-lookup"><span data-stu-id="313c0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="313c0-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="313c0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="313c0-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="313c0-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="313c0-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="313c0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="313c0-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="313c0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="313c0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="313c0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="313c0-123"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="313c0-123"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="313c0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="313c0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="313c0-125">**ABN \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="313c0-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="313c0-126">**ABN \_ GETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="313c0-126">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="313c0-127">**ABN \_ SETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="313c0-127">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




