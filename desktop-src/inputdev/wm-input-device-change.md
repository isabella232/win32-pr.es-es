---
title: Mensaje de WM_INPUT_DEVICE_CHANGE (Winuser. h)
description: Se envía a la ventana que se registró para recibir entradas sin procesar. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- Entrada de mouse y teclado de mensaje de WM_INPUT_DEVICE_CHANGE
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0edb6dbfbcfa9e024ba85613e3b7671e5f416397
ms.sourcegitcommit: 47d1f3859035a69340571bf50c3d36e0abeb2126
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "104078545"
---
# <a name="wm_input_device_change-message"></a><span data-ttu-id="28a87-105">Mensaje WM_INPUT_DEVICE_CHANGE</span><span class="sxs-lookup"><span data-stu-id="28a87-105">WM_INPUT_DEVICE_CHANGE message</span></span>

## <a name="description"></a><span data-ttu-id="28a87-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="28a87-106">Description</span></span>

<span data-ttu-id="28a87-107">Se envía a la ventana que se registró para recibir entradas sin procesar.</span><span class="sxs-lookup"><span data-stu-id="28a87-107">Sent to the window that registered to receive raw input.</span></span> 

<span data-ttu-id="28a87-108">Las notificaciones de entrada sin formato solo están disponibles después de que la aplicación llame a [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) con [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) marca.</span><span class="sxs-lookup"><span data-stu-id="28a87-108">Raw input notifications are available only after the application calls [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) flag.</span></span>

<span data-ttu-id="28a87-109">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="28a87-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a><span data-ttu-id="28a87-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28a87-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28a87-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28a87-111">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="28a87-112">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="28a87-112">Type: **WPARAM**</span></span>

<span data-ttu-id="28a87-113">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="28a87-113">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="28a87-114">Valor</span><span class="sxs-lookup"><span data-stu-id="28a87-114">Value</span></span>                    | <span data-ttu-id="28a87-115">Significado</span><span class="sxs-lookup"><span data-stu-id="28a87-115">Meaning</span></span>                                    |
|--------------------------|--------------------------------------------|
| <span data-ttu-id="28a87-116">**llegada de GIDC \_**</span><span class="sxs-lookup"><span data-stu-id="28a87-116">**GIDC\_ARRIVAL**</span></span> </br><span data-ttu-id="28a87-117">1</span><span class="sxs-lookup"><span data-stu-id="28a87-117">1</span></span> | <span data-ttu-id="28a87-118">Se ha agregado un nuevo dispositivo al sistema.</span><span class="sxs-lookup"><span data-stu-id="28a87-118">A new device has been added to the system.</span></span> </br> <span data-ttu-id="28a87-119">Puede llamar a [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) para obtener más información sobre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28a87-119">You can call [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) to get more information regarding the device.</span></span> |
| <span data-ttu-id="28a87-120">**eliminación de GIDC \_**</span><span class="sxs-lookup"><span data-stu-id="28a87-120">**GIDC\_REMOVAL**</span></span> </br><span data-ttu-id="28a87-121">2</span><span class="sxs-lookup"><span data-stu-id="28a87-121">2</span></span> | <span data-ttu-id="28a87-122">Se ha quitado un dispositivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="28a87-122">A device has been removed from the system.</span></span> |

</dd> <dt>

<span data-ttu-id="28a87-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28a87-123">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="28a87-124">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="28a87-124">Type: **LPARAM**</span></span>

<span data-ttu-id="28a87-125">**Identificador** del dispositivo de entrada sin formato.</span><span class="sxs-lookup"><span data-stu-id="28a87-125">The **HANDLE** to the raw input device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28a87-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28a87-126">Return value</span></span>

<span data-ttu-id="28a87-127">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="28a87-127">If an application processes this message, it should return zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="28a87-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="28a87-128">See also</span></span>

<span data-ttu-id="28a87-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="28a87-129">**Conceptual**</span></span>

[<span data-ttu-id="28a87-130">Entrada sin formato</span><span class="sxs-lookup"><span data-stu-id="28a87-130">Raw Input</span></span>](/windows/desktop/inputdev/raw-input)

<span data-ttu-id="28a87-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="28a87-131">**Reference**</span></span>

[<span data-ttu-id="28a87-132">RegisterRawInputDevices</span><span class="sxs-lookup"><span data-stu-id="28a87-132">RegisterRawInputDevices</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="28a87-133">Estructura RAWINPUTDEVICE</span><span class="sxs-lookup"><span data-stu-id="28a87-133">RAWINPUTDEVICE structure</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

