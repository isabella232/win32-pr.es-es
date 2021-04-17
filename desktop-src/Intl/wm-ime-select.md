---
description: Se envía a una aplicación cuando el sistema operativo está a punto de cambiar el IME actual. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: Mensaje de WM_IME_SELECT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686817"
---
# <a name="wm_ime_select-message"></a><span data-ttu-id="9382f-104">Mensaje de selección de \_ IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="9382f-104">WM\_IME\_SELECT message</span></span>

<span data-ttu-id="9382f-105">Se envía a una aplicación cuando el sistema operativo está a punto de cambiar el IME actual.</span><span class="sxs-lookup"><span data-stu-id="9382f-105">Sent to an application when the operating system is about to change the current IME.</span></span> <span data-ttu-id="9382f-106">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9382f-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
 WPARAM wParam,   
 LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="9382f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9382f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9382f-108">*identificador*</span><span class="sxs-lookup"><span data-stu-id="9382f-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="9382f-109">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="9382f-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="9382f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9382f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9382f-111">Indicador de selección.</span><span class="sxs-lookup"><span data-stu-id="9382f-111">Selection indicator.</span></span> <span data-ttu-id="9382f-112">Este parámetro especifica **true** si el IME indicado está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="9382f-112">This parameter specifies **TRUE** if the indicated IME is selected.</span></span> <span data-ttu-id="9382f-113">El parámetro se establece en **false** si el IME especificado ya no está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="9382f-113">The parameter is set to **FALSE** if the specified IME is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="9382f-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9382f-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9382f-115">Identificador de configuración regional de entrada asociado al IME.</span><span class="sxs-lookup"><span data-stu-id="9382f-115">Input locale identifier associated with the IME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9382f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9382f-116">Return value</span></span>

<span data-ttu-id="9382f-117">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="9382f-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9382f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9382f-118">Remarks</span></span>

<span data-ttu-id="9382f-119">Una aplicación que ha creado una ventana de IME debe pasar este mensaje a esa ventana para que pueda recuperar el controlador de distribución del teclado al IME recién seleccionado.</span><span class="sxs-lookup"><span data-stu-id="9382f-119">An application that has created an IME window should pass this message to that window so that it can retrieve the keyboard layout handle to the newly selected IME.</span></span>

<span data-ttu-id="9382f-120">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  procesa este mensaje pasando la información a la ventana IME predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9382f-120">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing the information to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="9382f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9382f-121">Requirements</span></span>



| <span data-ttu-id="9382f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9382f-122">Requirement</span></span> | <span data-ttu-id="9382f-123">Value</span><span class="sxs-lookup"><span data-stu-id="9382f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9382f-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9382f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9382f-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9382f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9382f-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9382f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9382f-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9382f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9382f-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9382f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9382f-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9382f-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9382f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="9382f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9382f-131">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="9382f-131">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="9382f-132">Mensajes del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="9382f-132">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
