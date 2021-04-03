---
description: Indica a la ventana del IME que muestre la ventana de estado. Para enviar este comando, la aplicación usa el mensaje de control de IME de WM \_ \_ con la configuración de parámetros que se muestra a continuación.
ms.assetid: 8c422592-ef59-4030-b684-81e4e552c6b0
title: Comando IMC_OPENSTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd0b5e19ef6a026459eedb050e9ac9587b5ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908128"
---
# <a name="imc_openstatuswindow-command"></a><span data-ttu-id="dc200-104">\_Comando IMC OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="dc200-104">IMC\_OPENSTATUSWINDOW command</span></span>

<span data-ttu-id="dc200-105">Indica a la ventana del IME que muestre la ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="dc200-105">Instructs the IME window to show the status window.</span></span> <span data-ttu-id="dc200-106">Para enviar este comando, la aplicación usa el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="dc200-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="dc200-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc200-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc200-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc200-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="dc200-109">Establezca en IMC \_ OPENSTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="dc200-109">Set to IMC\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="dc200-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc200-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="dc200-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dc200-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc200-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc200-112">Return Value</span></span>

<span data-ttu-id="dc200-113">Devuelve 0 si se realiza correctamente, o un valor distinto de cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dc200-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc200-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc200-114">Remarks</span></span>

<span data-ttu-id="dc200-115">Este comando se omite si el sistema operativo no está en el modo Mostrar estado de IME.</span><span class="sxs-lookup"><span data-stu-id="dc200-115">This command is ignored if the operating system is not in the show IME status mode.</span></span> <span data-ttu-id="dc200-116">El usuario puede establecer o borrar el modo Mostrar estado de IME en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="dc200-116">The user can set or clear the show IME status mode from the task bar.</span></span>

<span data-ttu-id="dc200-117">Si ya se muestra la ventana de estado, este comando no hace nada.</span><span class="sxs-lookup"><span data-stu-id="dc200-117">If the status window is already shown, this command does nothing.</span></span> <span data-ttu-id="dc200-118">Aunque la aplicación puede enviar este comando a la ventana del IME, la aplicación no recibe el comando [**imn \_ OPENSTATUSWINDOW**](imn-openstatuswindow.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="dc200-118">Although the application can send this command to the IME window, the application does not receive the corresponding [**IMN\_OPENSTATUSWINDOW**](imn-openstatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc200-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc200-119">Requirements</span></span>



| <span data-ttu-id="dc200-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc200-120">Requirement</span></span> | <span data-ttu-id="dc200-121">Value</span><span class="sxs-lookup"><span data-stu-id="dc200-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc200-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc200-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dc200-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dc200-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dc200-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc200-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dc200-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dc200-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dc200-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc200-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc200-127"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc200-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc200-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc200-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc200-129">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="dc200-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="dc200-130">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="dc200-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="dc200-131">**\_control IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="dc200-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




