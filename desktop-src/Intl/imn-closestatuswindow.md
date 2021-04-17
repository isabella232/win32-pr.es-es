---
description: Notifica a una aplicación cuando un IME está a punto de cerrar la ventana de estado. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: d59fdf76-50e7-4a59-b1bd-a12cdb0026f6
title: Código de notificación de IMN_CLOSESTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0347fb4b0d83a9e3891b9aea59d82ab81e2183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652706"
---
# <a name="imn_closestatuswindow-notification-code"></a><span data-ttu-id="e450c-104">Código de notificación de CLOSESTATUSWINDOW de IMN \_</span><span class="sxs-lookup"><span data-stu-id="e450c-104">IMN\_CLOSESTATUSWINDOW notification code</span></span>

<span data-ttu-id="e450c-105">Notifica a una aplicación cuando un IME está a punto de cerrar la ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="e450c-105">Notifies an application when an IME is about to close the status window.</span></span> <span data-ttu-id="e450c-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="e450c-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="e450c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e450c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e450c-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="e450c-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="e450c-109">Establézcalo en IMN \_ CLOSESTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="e450c-109">Set to IMN\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="e450c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="e450c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e450c-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e450c-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e450c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e450c-112">Return Value</span></span>

<span data-ttu-id="e450c-113">Este comando no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e450c-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e450c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e450c-114">Remarks</span></span>

<span data-ttu-id="e450c-115">Una aplicación debe procesar este comando si muestra la ventana de estado para el IME.</span><span class="sxs-lookup"><span data-stu-id="e450c-115">An application should process this command if it displays the status window for the IME.</span></span>

<span data-ttu-id="e450c-116">La ventana del IME cierra la ventana de estado al procesar este comando.</span><span class="sxs-lookup"><span data-stu-id="e450c-116">The IME window closes the status window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="e450c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e450c-117">Requirements</span></span>



| <span data-ttu-id="e450c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e450c-118">Requirement</span></span> | <span data-ttu-id="e450c-119">Value</span><span class="sxs-lookup"><span data-stu-id="e450c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e450c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e450c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e450c-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e450c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e450c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e450c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e450c-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e450c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e450c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e450c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e450c-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e450c-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e450c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e450c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e450c-127">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="e450c-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e450c-128">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="e450c-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="e450c-129">**\_notificación de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e450c-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




