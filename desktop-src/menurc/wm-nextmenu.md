---
title: Mensaje de WM_NEXTMENU (Winuser. h)
description: Se envía a una aplicación cuando se usa la tecla de dirección derecha o izquierda para cambiar entre la barra de menús y el menú del sistema.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecb8efe8c80a3355a30ab0abf28019f87b33963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997142"
---
# <a name="wm_nextmenu-message"></a><span data-ttu-id="66556-104">Mensaje de NEXTMENU de WM \_</span><span class="sxs-lookup"><span data-stu-id="66556-104">WM\_NEXTMENU message</span></span>

<span data-ttu-id="66556-105">Se envía a una aplicación cuando se usa la tecla de dirección derecha o izquierda para cambiar entre la barra de menús y el menú del sistema.</span><span class="sxs-lookup"><span data-stu-id="66556-105">Sent to an application when the right or left arrow key is used to switch between the menu bar and the system menu.</span></span>


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a><span data-ttu-id="66556-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66556-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66556-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66556-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66556-108">Código de la clave virtual de la clave.</span><span class="sxs-lookup"><span data-stu-id="66556-108">The virtual-key code of the key.</span></span> <span data-ttu-id="66556-109">Consulte [**códigos de tecla virtual**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="66556-109">See [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="66556-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66556-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66556-111">Puntero a una estructura [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) que contiene información sobre el menú que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="66556-111">A pointer to a [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) structure that contains information about the menu to be activated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66556-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66556-112">Remarks</span></span>

<span data-ttu-id="66556-113">Al responder a este mensaje, la aplicación puede especificar el menú al que se va a cambiar en el miembro **hmenuNext** de [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) y la ventana para recibir los mensajes de notificación de menú en el miembro **hwndNext** de la estructura **MDINEXTMENU** .</span><span class="sxs-lookup"><span data-stu-id="66556-113">In responding to this message, the application can specify the menu to switch to in the **hmenuNext** member of [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) and the window to receive the menu notification messages in the **hwndNext** member of the **MDINEXTMENU** structure.</span></span> <span data-ttu-id="66556-114">Debe establecer ambos miembros para que los cambios surtan efecto (son inicialmente **null**).</span><span class="sxs-lookup"><span data-stu-id="66556-114">You must set both members for the changes to take effect (they are initially **NULL**).</span></span>

## <a name="requirements"></a><span data-ttu-id="66556-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66556-115">Requirements</span></span>



| <span data-ttu-id="66556-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="66556-116">Requirement</span></span> | <span data-ttu-id="66556-117">Value</span><span class="sxs-lookup"><span data-stu-id="66556-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66556-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66556-118">Minimum supported client</span></span><br/> | <span data-ttu-id="66556-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="66556-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="66556-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66556-120">Minimum supported server</span></span><br/> | <span data-ttu-id="66556-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="66556-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="66556-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66556-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="66556-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66556-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66556-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="66556-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="66556-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="66556-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="66556-126">**MDINEXTMENU**</span><span class="sxs-lookup"><span data-stu-id="66556-126">**MDINEXTMENU**</span></span>](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

<span data-ttu-id="66556-127">**Vista**</span><span class="sxs-lookup"><span data-stu-id="66556-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="66556-128">Menús</span><span class="sxs-lookup"><span data-stu-id="66556-128">Menus</span></span>](menus.md)
</dt> </dl>

 

