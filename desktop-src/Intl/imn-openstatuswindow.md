---
description: Notifica a una aplicación cuando un IME está a punto de crear la ventana de estado. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: bbd85c72-aa78-4e1d-8a7a-490650b2d782
title: Código de notificación de IMN_OPENSTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca33771d1474c2f2ac78551a31545cecc2e513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687615"
---
# <a name="imn_openstatuswindow-notification-code"></a><span data-ttu-id="613ce-104">Código de notificación de OPENSTATUSWINDOW de IMN \_</span><span class="sxs-lookup"><span data-stu-id="613ce-104">IMN\_OPENSTATUSWINDOW notification code</span></span>

<span data-ttu-id="613ce-105">Notifica a una aplicación cuando un IME está a punto de crear la ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="613ce-105">Notifies an application when an IME is about to create the status window.</span></span> <span data-ttu-id="613ce-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="613ce-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="613ce-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="613ce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="613ce-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="613ce-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="613ce-109">Establézcalo en IMN \_ OPENSTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="613ce-109">Set to IMN\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="613ce-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="613ce-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="613ce-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="613ce-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="613ce-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="613ce-112">Return Value</span></span>

<span data-ttu-id="613ce-113">Este comando no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="613ce-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="613ce-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="613ce-114">Remarks</span></span>

<span data-ttu-id="613ce-115">Una aplicación procesa este comando para mostrar la ventana de estado para el IME.</span><span class="sxs-lookup"><span data-stu-id="613ce-115">An application processes this command to display the status window for the IME by itself.</span></span>

<span data-ttu-id="613ce-116">La ventana del IME crea una ventana de estado al procesar este comando y establece las cadenas que se van a mostrar en la ventana en el contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="613ce-116">The IME window creates a status window when it processes this command and sets the strings to display in the window into the input context.</span></span> <span data-ttu-id="613ce-117">Las aplicaciones pueden obtener información sobre la ventana de estado mediante la función [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="613ce-117">Applications can get information about the status window by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="613ce-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="613ce-118">Requirements</span></span>



| <span data-ttu-id="613ce-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="613ce-119">Requirement</span></span> | <span data-ttu-id="613ce-120">Value</span><span class="sxs-lookup"><span data-stu-id="613ce-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="613ce-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="613ce-121">Minimum supported client</span></span><br/> | <span data-ttu-id="613ce-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="613ce-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="613ce-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="613ce-123">Minimum supported server</span></span><br/> | <span data-ttu-id="613ce-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="613ce-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="613ce-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="613ce-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="613ce-126"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="613ce-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="613ce-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="613ce-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="613ce-128">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="613ce-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="613ce-129">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="613ce-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="613ce-130">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="613ce-130">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="613ce-131">**\_notificación de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="613ce-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




