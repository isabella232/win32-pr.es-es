---
title: Mensaje de WM_MENUDRAG (Winuser. h)
description: Se envía al propietario de un menú de arrastrar y colocar cuando el usuario arrastra un elemento de menú.
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- WM_MENUDRAG menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67e83c41576a716d292187df4cb08fa803271c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714650"
---
# <a name="wm_menudrag-message"></a><span data-ttu-id="06f95-104">Mensaje de MENUDRAG de WM \_</span><span class="sxs-lookup"><span data-stu-id="06f95-104">WM\_MENUDRAG message</span></span>

<span data-ttu-id="06f95-105">Se envía al propietario de un menú de arrastrar y colocar cuando el usuario arrastra un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="06f95-105">Sent to the owner of a drag-and-drop menu when the user drags a menu item.</span></span>


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a><span data-ttu-id="06f95-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06f95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06f95-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06f95-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06f95-108">Posición del elemento donde comenzó la operación de arrastre.</span><span class="sxs-lookup"><span data-stu-id="06f95-108">The position of the item where the drag operation began.</span></span>

</dd> <dt>

<span data-ttu-id="06f95-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06f95-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06f95-110">Identificador del menú que contiene el elemento.</span><span class="sxs-lookup"><span data-stu-id="06f95-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06f95-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06f95-111">Return value</span></span>

<span data-ttu-id="06f95-112">La aplicación debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="06f95-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="06f95-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06f95-113">Return code/value</span></span>                                                                                                                                   | <span data-ttu-id="06f95-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="06f95-114">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06f95-115"><dt>**MND \_ CONTINUAR**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="06f95-115"><dt>**MND\_CONTINUE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="06f95-116">El menú debe permanecer activo.</span><span class="sxs-lookup"><span data-stu-id="06f95-116">Menu should remain active.</span></span> <span data-ttu-id="06f95-117">Si se suelta el mouse, debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="06f95-117">If the mouse is released, it should be ignored.</span></span><br/> |
| <dl> <span data-ttu-id="06f95-118"><dt>**MND \_ ENDMENU**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="06f95-118"><dt>**MND\_ENDMENU**</dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="06f95-119">El menú debe finalizar.</span><span class="sxs-lookup"><span data-stu-id="06f95-119">Menu should be ended.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="06f95-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06f95-120">Remarks</span></span>

<span data-ttu-id="06f95-121">La aplicación puede llamar a la función [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) en respuesta a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="06f95-121">The application can call the [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) function in response to this message.</span></span>

<span data-ttu-id="06f95-122">Para crear un menú de arrastrar y colocar, llame a [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) con **mns \_ DRAGDROP**.</span><span class="sxs-lookup"><span data-stu-id="06f95-122">To create a drag-and-drop menu, call [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) with **MNS\_DRAGDROP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="06f95-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06f95-123">Requirements</span></span>



| <span data-ttu-id="06f95-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="06f95-124">Requirement</span></span> | <span data-ttu-id="06f95-125">Value</span><span class="sxs-lookup"><span data-stu-id="06f95-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06f95-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06f95-126">Minimum supported client</span></span><br/> | <span data-ttu-id="06f95-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="06f95-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="06f95-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06f95-128">Minimum supported server</span></span><br/> | <span data-ttu-id="06f95-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="06f95-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="06f95-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06f95-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="06f95-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06f95-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06f95-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="06f95-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="06f95-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="06f95-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="06f95-134">**SetMenuInfo**</span><span class="sxs-lookup"><span data-stu-id="06f95-134">**SetMenuInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

<span data-ttu-id="06f95-135">**Vista**</span><span class="sxs-lookup"><span data-stu-id="06f95-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="06f95-136">Menús</span><span class="sxs-lookup"><span data-stu-id="06f95-136">Menus</span></span>](menus.md)
</dt> </dl>

 

