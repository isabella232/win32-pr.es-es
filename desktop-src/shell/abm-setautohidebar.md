---
description: Registra o anula el registro de un Appbar de ocultación para un borde determinado de la pantalla. Si el sistema tiene varios monitores, se utiliza el monitor que contiene la barra de tareas principal.
title: Mensaje de ABM_SETAUTOHIDEBAR (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0cbd6c9c-e83f-41f8-91ed-81afaa24f524
api_name:
- ABM_SETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 53ca89008dda1233d12a7f0a9588803776ba1181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984386"
---
# <a name="abm_setautohidebar-message"></a><span data-ttu-id="a5d44-104">ABN \_ SETAUTOHIDEBAR</span><span class="sxs-lookup"><span data-stu-id="a5d44-104">ABM\_SETAUTOHIDEBAR message</span></span>

<span data-ttu-id="a5d44-105">Registra o anula el registro de un Appbar de ocultación para un borde determinado de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a5d44-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="a5d44-106">Si el sistema tiene varios monitores, se utiliza el monitor que contiene la barra de tareas principal.</span><span class="sxs-lookup"><span data-stu-id="a5d44-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="a5d44-107">Para registrar o anular el registro de un Appbar de ocultación automáticamente en un monitor específico, use [**ABN \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md).</span><span class="sxs-lookup"><span data-stu-id="a5d44-107">To register or unregister an autohide appbar on a specific monitor, use [**ABM\_SETAUTOHIDEBAREX**](abm-setautohidebarex.md).</span></span>

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="a5d44-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5d44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5d44-109">*pabd*</span><span class="sxs-lookup"><span data-stu-id="a5d44-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="a5d44-110">Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="a5d44-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="a5d44-111">Establezca el miembro **lParam** en **true** para registrar el Appbar o **false** para anular su registro.</span><span class="sxs-lookup"><span data-stu-id="a5d44-111">Set the **lParam** member to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="a5d44-112">Debe especificar los miembros **cbSize**, **hWnd**, **uEdge** y **lParam** al enviar este mensaje. se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="a5d44-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5d44-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5d44-113">Return value</span></span>

<span data-ttu-id="a5d44-114">Devuelve **true** si es correcto, o **false** si se produce un error o si ya se ha registrado un Appbar de ocultación para el borde especificado.</span><span class="sxs-lookup"><span data-stu-id="a5d44-114">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5d44-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5d44-115">Remarks</span></span>

<span data-ttu-id="a5d44-116">El sistema solo permite un Appbar de ocultación automáticamente para cada borde de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a5d44-116">The system allows only one autohide appbar for each edge of the screen.</span></span> <span data-ttu-id="a5d44-117">Esto se determina cuando se establece el miembro **uEdge** de la estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="a5d44-117">This is determined when the member **uEdge** of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5d44-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5d44-118">Requirements</span></span>



| <span data-ttu-id="a5d44-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5d44-119">Requirement</span></span> | <span data-ttu-id="a5d44-120">Value</span><span class="sxs-lookup"><span data-stu-id="a5d44-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d44-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5d44-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a5d44-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a5d44-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a5d44-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5d44-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a5d44-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a5d44-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5d44-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5d44-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5d44-126"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5d44-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5d44-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5d44-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5d44-128">**ABN \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="a5d44-128">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="a5d44-129">**ABN \_ GETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="a5d44-129">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="a5d44-130">**ABN \_ SETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="a5d44-130">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




