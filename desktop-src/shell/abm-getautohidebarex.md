---
description: Recupera el identificador del Appbar de ocultación automático asociado a un borde de la pantalla. Este mensaje amplía ABN \_ GETAUTOHIDEBAR, ya que permite especificar un monitor determinado para su uso en varias situaciones de supervisión.
title: Mensaje de ABM_GETAUTOHIDEBAREX (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ef95739a1031efb199e6acd99686e0858a9630e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987517"
---
# <a name="abm_getautohidebarex-message"></a><span data-ttu-id="0b82c-104">ABN \_ GETAUTOHIDEBAREX</span><span class="sxs-lookup"><span data-stu-id="0b82c-104">ABM\_GETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="0b82c-105">Recupera el identificador del Appbar de ocultación automático asociado a un borde de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="0b82c-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="0b82c-106">Este mensaje amplía [**ABN \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) , ya que permite especificar un monitor determinado para su uso en varias situaciones de supervisión.</span><span class="sxs-lookup"><span data-stu-id="0b82c-106">This message extends [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="0b82c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b82c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b82c-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="0b82c-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="0b82c-109">Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que especifica el borde y el monitor de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="0b82c-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge and monitor.</span></span> <span data-ttu-id="0b82c-110">Debe especificar los miembros **cbSize**, **uEdge** y **RC** al enviar este mensaje. se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="0b82c-110">You must specify the **cbSize**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b82c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b82c-111">Return value</span></span>

<span data-ttu-id="0b82c-112">Devuelve el identificador del Appbar de ocultación automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0b82c-112">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="0b82c-113">El valor devuelto es **null** si se produce un error o si no hay ningún Appbar de ocultación automático asociado al borde determinado del monitor determinado.</span><span class="sxs-lookup"><span data-stu-id="0b82c-113">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge of the given monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b82c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b82c-114">Requirements</span></span>



| <span data-ttu-id="0b82c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b82c-115">Requirement</span></span> | <span data-ttu-id="0b82c-116">Value</span><span class="sxs-lookup"><span data-stu-id="0b82c-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b82c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b82c-117">Header</span></span><br/> | <dl> <span data-ttu-id="0b82c-118"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b82c-118"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b82c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b82c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b82c-120">**ABN \_ GETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="0b82c-120">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="0b82c-121">**ABN \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="0b82c-121">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="0b82c-122">**ABN \_ SETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="0b82c-122">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




