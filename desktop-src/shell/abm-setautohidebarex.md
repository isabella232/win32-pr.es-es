---
description: Registra o anula el registro de un Appbar de ocultación para un borde determinado de la pantalla. Este mensaje amplía ABN \_ SETAUTOHIDEBAR, ya que permite especificar un monitor determinado para su uso en varias situaciones de supervisión.
title: Mensaje de ABM_SETAUTOHIDEBAREX (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C437727C-3FF6-4598-9D81-A39FCC2EF1C4
api_name:
- ABM_SETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba4e1474d3b57465fa68446fd7ab787c9a62570b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104998887"
---
# <a name="abm_setautohidebarex-message"></a><span data-ttu-id="11c8d-104">ABN \_ SETAUTOHIDEBAREX</span><span class="sxs-lookup"><span data-stu-id="11c8d-104">ABM\_SETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="11c8d-105">Registra o anula el registro de un Appbar de ocultación para un borde determinado de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="11c8d-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="11c8d-106">Este mensaje amplía [**ABN \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) , ya que permite especificar un monitor determinado para su uso en varias situaciones de supervisión.</span><span class="sxs-lookup"><span data-stu-id="11c8d-106">This message extends [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="11c8d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11c8d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11c8d-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="11c8d-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="11c8d-109">Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="11c8d-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="11c8d-110">Establezca el miembro **lParam** en **true** para registrar el Appbar o **false** para anular su registro.</span><span class="sxs-lookup"><span data-stu-id="11c8d-110">Set the **lParam** member is to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="11c8d-111">Debe especificar los miembros **cbSize**, **hWnd**, **uEdge**, **RC** y **lParam** al enviar este mensaje. se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="11c8d-111">You must specify the **cbSize**, **hWnd**, **uEdge**, **rc**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11c8d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11c8d-112">Return value</span></span>

<span data-ttu-id="11c8d-113">Devuelve **true** si es correcto, o **false** si se produce un error o si ya se ha registrado un Appbar de ocultación para el borde dado en el monitor determinado.</span><span class="sxs-lookup"><span data-stu-id="11c8d-113">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge on the given monitor.</span></span>

## <a name="remarks"></a><span data-ttu-id="11c8d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11c8d-114">Remarks</span></span>

<span data-ttu-id="11c8d-115">El sistema solo permite un Appbar de ocultación automáticamente para cada borde de cada monitor.</span><span class="sxs-lookup"><span data-stu-id="11c8d-115">The system allows only one autohide appbar for each edge of each monitor.</span></span> <span data-ttu-id="11c8d-116">El monitor viene determinado por el miembro **RC** y el límite viene determinado por el miembro **uEdge** de la estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="11c8d-116">The monitor is determined by the **rc** member and the edge is determined by the **uEdge** member of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="11c8d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11c8d-117">Requirements</span></span>



| <span data-ttu-id="11c8d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="11c8d-118">Requirement</span></span> | <span data-ttu-id="11c8d-119">Value</span><span class="sxs-lookup"><span data-stu-id="11c8d-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11c8d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11c8d-120">Header</span></span><br/> | <dl> <span data-ttu-id="11c8d-121"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="11c8d-121"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11c8d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="11c8d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c8d-123">**ABN \_ GETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="11c8d-123">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="11c8d-124">**ABN \_ GETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="11c8d-124">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="11c8d-125">**ABN \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="11c8d-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> </dl>

 

 




