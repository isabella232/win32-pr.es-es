---
description: Indica a una ventana de IME que obtenga la posición de la ventana de estado. Para enviar este comando, la aplicación usa el mensaje de control de IME de WM \_ \_ con la configuración de parámetros que se muestra a continuación.
ms.assetid: 59c7baae-1b8a-4761-9814-31afd8d39691
title: Comando IMC_GETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd17c5787d9ef8c787e62a556afa2f136bd65c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686923"
---
# <a name="imc_getstatuswindowpos-command"></a><span data-ttu-id="5e414-104">\_Comando IMC GETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="5e414-104">IMC\_GETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="5e414-105">Indica a una ventana de IME que obtenga la posición de la ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="5e414-105">Instructs an IME window to get the position of the status window.</span></span> <span data-ttu-id="5e414-106">Para enviar este comando, la aplicación usa el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="5e414-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="5e414-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e414-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e414-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e414-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="5e414-109">Establezca en IMC \_ GETSTATUSWINDOWPOS.</span><span class="sxs-lookup"><span data-stu-id="5e414-109">Set to IMC\_GETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="5e414-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e414-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="5e414-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5e414-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e414-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e414-112">Return Value</span></span>

<span data-ttu-id="5e414-113">Devuelve una estructura de [**puntos**](/previous-versions//dd162808(v=vs.85)) que contiene la coordenada x y la coordenada y de la posición de la ventana de estado en coordenadas de la pantalla, con respecto a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="5e414-113">Returns a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the status window position in screen coordinates, relative to the upper left corner of the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e414-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e414-114">Requirements</span></span>



| <span data-ttu-id="5e414-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e414-115">Requirement</span></span> | <span data-ttu-id="5e414-116">Value</span><span class="sxs-lookup"><span data-stu-id="5e414-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e414-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e414-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5e414-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5e414-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5e414-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e414-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5e414-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5e414-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5e414-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e414-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e414-122"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e414-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e414-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e414-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e414-124">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="5e414-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="5e414-125">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="5e414-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="5e414-126">**\_control IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5e414-126">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
