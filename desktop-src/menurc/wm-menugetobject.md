---
title: Mensaje de WM_MENUGETOBJECT (Winuser. h)
description: Se envía al propietario de un menú de arrastrar y colocar cuando el cursor del Mouse entra en un elemento de menú o se mueve desde el centro del elemento hasta la parte superior o inferior del elemento.
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- WM_MENUGETOBJECT menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e124c7f2757a0d6d1d2ac0904052b6d3c255ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535553"
---
# <a name="wm_menugetobject-message"></a><span data-ttu-id="04433-104">Mensaje de MENUGETOBJECT de WM \_</span><span class="sxs-lookup"><span data-stu-id="04433-104">WM\_MENUGETOBJECT message</span></span>

<span data-ttu-id="04433-105">Se envía al propietario de un menú de arrastrar y colocar cuando el cursor del Mouse entra en un elemento de menú o se mueve desde el centro del elemento hasta la parte superior o inferior del elemento.</span><span class="sxs-lookup"><span data-stu-id="04433-105">Sent to the owner of a drag-and-drop menu when the mouse cursor enters a menu item or moves from the center of the item to the top or bottom of the item.</span></span>


```C++
#define WM_MENUGETOBJECT                0x0124
```



## <a name="parameters"></a><span data-ttu-id="04433-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04433-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04433-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04433-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04433-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="04433-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04433-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04433-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04433-110">Puntero a una estructura [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) .</span><span class="sxs-lookup"><span data-stu-id="04433-110">A pointer to a [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04433-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04433-111">Return value</span></span>

<span data-ttu-id="04433-112">La aplicación debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="04433-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="04433-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04433-113">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="04433-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="04433-114">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="04433-115"><dt>**MNGO \_ NoError**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="04433-115"><dt>**MNGO\_NOERROR**</dt> <dt>0x00000001</dt></span></span> </dl>     | <span data-ttu-id="04433-116">Se devolvió un puntero de interfaz en el miembro **pvObj** de [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)</span><span class="sxs-lookup"><span data-stu-id="04433-116">An interface pointer was returned in the **pvObj** member of [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)</span></span><br/> |
| <dl> <span data-ttu-id="04433-117"><dt>**MNGO \_ Nointerface**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="04433-117"><dt>**MNGO\_NOINTERFACE**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="04433-118">No se admite la interfaz.</span><span class="sxs-lookup"><span data-stu-id="04433-118">The interface is not supported.</span></span><br/>                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="04433-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04433-119">Requirements</span></span>



| <span data-ttu-id="04433-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="04433-120">Requirement</span></span> | <span data-ttu-id="04433-121">Value</span><span class="sxs-lookup"><span data-stu-id="04433-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04433-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04433-122">Minimum supported client</span></span><br/> | <span data-ttu-id="04433-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="04433-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="04433-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04433-124">Minimum supported server</span></span><br/> | <span data-ttu-id="04433-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04433-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="04433-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04433-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="04433-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04433-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04433-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="04433-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04433-129">Información general sobre menús</span><span class="sxs-lookup"><span data-stu-id="04433-129">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





