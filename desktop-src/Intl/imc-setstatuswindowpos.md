---
description: Indica a una ventana del IME que establezca la posición de la ventana de estado. Para enviar este comando, la aplicación usa el \_ mensaje de control de IME de WM con la configuración de parámetros, \_ como se muestra a continuación.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: Comando IMC_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c57eef1a4748bb58018ee47aaee21eb677016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082195"
---
# <a name="imc_setstatuswindowpos-command"></a><span data-ttu-id="abe21-104">\_Comando IMC SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="abe21-104">IMC\_SETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="abe21-105">Indica a una ventana del IME que establezca la posición de la ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="abe21-105">Instructs an IME window to set the position of the status window.</span></span> <span data-ttu-id="abe21-106">Para enviar este comando, la aplicación usa el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="abe21-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="abe21-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="abe21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abe21-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="abe21-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="abe21-109">Establezca en IMC \_ SETSTATUSWINDOWPOS.</span><span class="sxs-lookup"><span data-stu-id="abe21-109">Set to IMC\_SETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="abe21-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="abe21-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="abe21-111">Puntero a una estructura de [**puntos**](/previous-versions//dd162808(v=vs.85)) que contiene la coordenada x y la coordenada y de la posición de la ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="abe21-111">Pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the position of the status window.</span></span> <span data-ttu-id="abe21-112">Las coordenadas están en coordenadas de pantalla, con respecto a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="abe21-112">The coordinates are in screen coordinates, relative to the upper left corner of the display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abe21-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="abe21-113">Return Value</span></span>

<span data-ttu-id="abe21-114">Devuelve 0 si se realiza correctamente, o un valor distinto de cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="abe21-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="abe21-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abe21-115">Requirements</span></span>



| <span data-ttu-id="abe21-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="abe21-116">Requirement</span></span> | <span data-ttu-id="abe21-117">Value</span><span class="sxs-lookup"><span data-stu-id="abe21-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abe21-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abe21-118">Minimum supported client</span></span><br/> | <span data-ttu-id="abe21-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="abe21-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="abe21-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abe21-120">Minimum supported server</span></span><br/> | <span data-ttu-id="abe21-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="abe21-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="abe21-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abe21-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="abe21-123"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="abe21-123"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abe21-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="abe21-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe21-125">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="abe21-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="abe21-126">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="abe21-126">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="abe21-127">**\_control IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="abe21-127">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
