---
description: El mensaje de DEVMODECHANGE de WM \_ se envía a todas las ventanas de nivel superior cada vez que el usuario cambia la configuración del modo de dispositivo.
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: Mensaje de WM_DEVMODECHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985806"
---
# <a name="wm_devmodechange-message"></a><span data-ttu-id="35343-103">Mensaje de DEVMODECHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="35343-103">WM\_DEVMODECHANGE message</span></span>

<span data-ttu-id="35343-104">El mensaje de **\_ DEVMODECHANGE de WM** se envía a todas las ventanas de nivel superior cada vez que el usuario cambia la configuración del modo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35343-104">The **WM\_DEVMODECHANGE** message is sent to all top-level windows whenever the user changes device-mode settings.</span></span>

<span data-ttu-id="35343-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="35343-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="35343-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35343-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35343-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="35343-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="35343-108">Identificador a una ventana.</span><span class="sxs-lookup"><span data-stu-id="35343-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="35343-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="35343-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="35343-110">DEVMODECHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="35343-110">WM\_DEVMODECHANGE</span></span>

</dd> <dt>

<span data-ttu-id="35343-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35343-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35343-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="35343-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35343-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35343-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35343-114">Puntero a una cadena que especifica el nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35343-114">A pointer to a string that specifies the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35343-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35343-115">Return value</span></span>

<span data-ttu-id="35343-116">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="35343-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="35343-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35343-117">Remarks</span></span>

<span data-ttu-id="35343-118">Este mensaje no se puede enviar directamente a una ventana.</span><span class="sxs-lookup"><span data-stu-id="35343-118">This message cannot be sent directly to a window.</span></span> <span data-ttu-id="35343-119">Para enviar el mensaje de **\_ DEVMODECHANGE de WM** a todas las ventanas de nivel superior, use la función [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) con el parámetro *hWnd* establecido en la \_ difusión HWND.</span><span class="sxs-lookup"><span data-stu-id="35343-119">To send the **WM\_DEVMODECHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hWnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="35343-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35343-120">Requirements</span></span>



| <span data-ttu-id="35343-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="35343-121">Requirement</span></span> | <span data-ttu-id="35343-122">Value</span><span class="sxs-lookup"><span data-stu-id="35343-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35343-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35343-123">Minimum supported client</span></span><br/> | <span data-ttu-id="35343-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="35343-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="35343-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35343-125">Minimum supported server</span></span><br/> | <span data-ttu-id="35343-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="35343-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="35343-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35343-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="35343-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35343-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35343-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="35343-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35343-130">Introducción a los contextos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="35343-130">Device Contexts Overview</span></span>](device-contexts.md)
</dt> <dt>

[<span data-ttu-id="35343-131">Mensajes de contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="35343-131">Device Context Messages</span></span>](device-context-messages.md)
</dt> </dl>

 

 
