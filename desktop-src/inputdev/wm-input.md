---
title: Mensaje de WM_INPUT (Winuser. h)
description: Se envía a la ventana que obtiene la entrada sin formato. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- Entrada de mouse y teclado de mensaje de WM_INPUT
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422194"
---
# <a name="wm_input-message"></a><span data-ttu-id="6a0b0-105">Mensaje de entrada de WM \_</span><span class="sxs-lookup"><span data-stu-id="6a0b0-105">WM\_INPUT message</span></span>

<span data-ttu-id="6a0b0-106">Se envía a la ventana que obtiene la entrada sin formato.</span><span class="sxs-lookup"><span data-stu-id="6a0b0-106">Sent to the window that is getting raw input.</span></span>

<span data-ttu-id="6a0b0-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6a0b0-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a><span data-ttu-id="6a0b0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a0b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a0b0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6a0b0-109">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="6a0b0-110">Código de entrada.</span><span class="sxs-lookup"><span data-stu-id="6a0b0-110">The input code.</span></span> <span data-ttu-id="6a0b0-111">Use la macro [**Get \_ RAWINPUT \_ code \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="6a0b0-111">Use [**GET\_RAWINPUT\_CODE\_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) macro to get the value.</span></span>

<span data-ttu-id="6a0b0-112">Puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="6a0b0-112">Can be one of the following values:</span></span>

| <span data-ttu-id="6a0b0-113">Value</span><span class="sxs-lookup"><span data-stu-id="6a0b0-113">Value</span></span> | <span data-ttu-id="6a0b0-114">Significado</span><span class="sxs-lookup"><span data-stu-id="6a0b0-114">Meaning</span></span> |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <span data-ttu-id="6a0b0-115"><dt>**RIM \_ ENTRADA**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6a0b0-115"><dt>**RIM\_INPUT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="6a0b0-116">La entrada se produjo mientras la aplicación estaba en primer plano.</span><span class="sxs-lookup"><span data-stu-id="6a0b0-116">Input occurred while the application was in the foreground.</span></span> </br> <span data-ttu-id="6a0b0-117">La aplicación debe llamar a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para que el sistema pueda realizar la limpieza.</span><span class="sxs-lookup"><span data-stu-id="6a0b0-117">The application must call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) so the system can perform cleanup.</span></span> |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <span data-ttu-id="6a0b0-118"><dt>**RIM \_ INPUTSINK**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6a0b0-118"><dt>**RIM\_INPUTSINK**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="6a0b0-119">La entrada se produjo mientras la aplicación no estaba en primer plano.</span><span class="sxs-lookup"><span data-stu-id="6a0b0-119">Input occurred while the application was not in the foreground.</span></span> |

</dd> <dt>

<span data-ttu-id="6a0b0-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a0b0-120">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="6a0b0-121">Identificador de **HRAWINPUT** de la estructura [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) que contiene la entrada sin formato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a0b0-121">A **HRAWINPUT** handle to the [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structure that contains the raw input from the device.</span></span> <span data-ttu-id="6a0b0-122">Para obtener los datos sin procesar, use este identificador en la llamada a [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).</span><span class="sxs-lookup"><span data-stu-id="6a0b0-122">To get the raw data, use this handle in the call to [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a0b0-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a0b0-123">Return value</span></span>

<span data-ttu-id="6a0b0-124">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="6a0b0-124">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a0b0-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a0b0-125">Remarks</span></span>

<span data-ttu-id="6a0b0-126">La entrada sin formato solo está disponible cuando la aplicación llama a [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) con especificaciones de dispositivo válidas.</span><span class="sxs-lookup"><span data-stu-id="6a0b0-126">Raw input is available only when the application calls [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with valid device specifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a0b0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a0b0-127">Requirements</span></span>

| <span data-ttu-id="6a0b0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a0b0-128">Requirement</span></span> | <span data-ttu-id="6a0b0-129">Value</span><span class="sxs-lookup"><span data-stu-id="6a0b0-129">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="6a0b0-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a0b0-130">Minimum supported client</span></span> | <span data-ttu-id="6a0b0-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6a0b0-131">Windows XP \[desktop apps only\]</span></span> |
| <span data-ttu-id="6a0b0-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a0b0-132">Minimum supported server</span></span> | <span data-ttu-id="6a0b0-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a0b0-133">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="6a0b0-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a0b0-134">Header</span></span> | <dl> <span data-ttu-id="6a0b0-135"><dt>**Winuser. h (incluir Windows. h)**</dt></span><span class="sxs-lookup"><span data-stu-id="6a0b0-135"><dt>**Winuser.h (include Windows.h)** </dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="6a0b0-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a0b0-136">See also</span></span>

<span data-ttu-id="6a0b0-137">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="6a0b0-137">**Reference**</span></span>

[<span data-ttu-id="6a0b0-138">**GetRawInputData**</span><span class="sxs-lookup"><span data-stu-id="6a0b0-138">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[<span data-ttu-id="6a0b0-139">**RegisterRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="6a0b0-139">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="6a0b0-140">**RAWINPUT**</span><span class="sxs-lookup"><span data-stu-id="6a0b0-140">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)

[<span data-ttu-id="6a0b0-141">**OBTENCIÓN \_ del \_ código RAWINPUT \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="6a0b0-141">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

<span data-ttu-id="6a0b0-142">**Vista**</span><span class="sxs-lookup"><span data-stu-id="6a0b0-142">**Conceptual**</span></span>

[<span data-ttu-id="6a0b0-143">Entrada sin formato</span><span class="sxs-lookup"><span data-stu-id="6a0b0-143">Raw Input</span></span>](raw-input.md)
