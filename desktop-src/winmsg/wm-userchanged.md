---
description: Se envía a todas las ventanas después de que el usuario haya iniciado sesión o desactivado. Cuando el usuario inicia o cierra sesión, el sistema actualiza la configuración específica del usuario. El sistema envía este mensaje inmediatamente después de actualizar la configuración.
title: Mensaje de WM_USERCHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14458bdafa0bbf4421c67db8102491db4e1fe6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002870"
---
# <a name="wm_userchanged-message"></a><span data-ttu-id="7930e-105">Mensaje de USERCHANGED de WM \_</span><span class="sxs-lookup"><span data-stu-id="7930e-105">WM\_USERCHANGED message</span></span>

<span data-ttu-id="7930e-106">Se envía a todas las ventanas después de que el usuario haya iniciado sesión o desactivado.</span><span class="sxs-lookup"><span data-stu-id="7930e-106">Sent to all windows after the user has logged on or off.</span></span> <span data-ttu-id="7930e-107">Cuando el usuario inicia o cierra sesión, el sistema actualiza la configuración específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="7930e-107">When the user logs on or off, the system updates the user-specific settings.</span></span> <span data-ttu-id="7930e-108">El sistema envía este mensaje inmediatamente después de actualizar la configuración.</span><span class="sxs-lookup"><span data-stu-id="7930e-108">The system sends this message immediately after updating the settings.</span></span>

<span data-ttu-id="7930e-109">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7930e-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="7930e-110">Este mensaje no es compatible con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7930e-110">This message is not supported as of Windows Vista.</span></span>

 


```C++
#define WM_USERCHANGED                  0x0054
```



## <a name="parameters"></a><span data-ttu-id="7930e-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7930e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7930e-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7930e-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7930e-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="7930e-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7930e-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7930e-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7930e-115">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="7930e-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7930e-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7930e-116">Return value</span></span>

<span data-ttu-id="7930e-117">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="7930e-117">Type: **LRESULT**</span></span>

<span data-ttu-id="7930e-118">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="7930e-118">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7930e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7930e-119">Requirements</span></span>



| <span data-ttu-id="7930e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7930e-120">Requirement</span></span> | <span data-ttu-id="7930e-121">Value</span><span class="sxs-lookup"><span data-stu-id="7930e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7930e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7930e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7930e-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7930e-123">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7930e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7930e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7930e-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7930e-125">None supported</span></span><br/>                                                                                |
| <span data-ttu-id="7930e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7930e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7930e-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7930e-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7930e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7930e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7930e-129">Información general de Windows</span><span class="sxs-lookup"><span data-stu-id="7930e-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
