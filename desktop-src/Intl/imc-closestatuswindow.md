---
description: Indica a la ventana del IME que oculte la ventana de estado. Para enviar este comando, la aplicación usa el mensaje de control de IME de WM \_ \_ con la configuración de parámetros que se muestra a continuación.
ms.assetid: e3da5962-a652-409e-b0ec-eb93671049b4
title: Comando IMC_CLOSESTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207f04d53f269318f87ed11038cbd6817d5e607e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913881"
---
# <a name="imc_closestatuswindow-command"></a><span data-ttu-id="285a5-104">\_Comando IMC CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="285a5-104">IMC\_CLOSESTATUSWINDOW command</span></span>

<span data-ttu-id="285a5-105">Indica a la ventana del IME que oculte la ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="285a5-105">Instructs the IME window to hide the status window.</span></span> <span data-ttu-id="285a5-106">Para enviar este comando, la aplicación usa el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="285a5-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="285a5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="285a5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="285a5-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="285a5-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="285a5-109">Establezca en IMC \_ CLOSESTATUSWINDOW.</span><span class="sxs-lookup"><span data-stu-id="285a5-109">Set to IMC\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="285a5-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="285a5-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="285a5-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="285a5-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="285a5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="285a5-112">Return Value</span></span>

<span data-ttu-id="285a5-113">Devuelve 0 si se realiza correctamente, o un valor distinto de cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="285a5-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="285a5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="285a5-114">Remarks</span></span>

<span data-ttu-id="285a5-115">Cuando la ventana de estado de IME ya está oculta, este comando no hace nada.</span><span class="sxs-lookup"><span data-stu-id="285a5-115">When the IME status window is already hidden, this command does nothing.</span></span> <span data-ttu-id="285a5-116">Aunque una aplicación puede enviar este comando a la ventana del IME, la aplicación no recibe el comando [imn \_ CLOSESTATUSWINDOW](imn-closestatuswindow.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="285a5-116">Although an application can send this command to the IME window, the application does not receive the corresponding [IMN\_CLOSESTATUSWINDOW](imn-closestatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="285a5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="285a5-117">Requirements</span></span>



| <span data-ttu-id="285a5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="285a5-118">Requirement</span></span> | <span data-ttu-id="285a5-119">Value</span><span class="sxs-lookup"><span data-stu-id="285a5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285a5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="285a5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="285a5-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="285a5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="285a5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="285a5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="285a5-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="285a5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="285a5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="285a5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="285a5-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="285a5-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="285a5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="285a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="285a5-127">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="285a5-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="285a5-128">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="285a5-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 




