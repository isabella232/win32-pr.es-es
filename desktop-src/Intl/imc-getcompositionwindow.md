---
description: Indica a una ventana de IME que obtenga la posición de la ventana de composición. Para enviar este comando, la aplicación usa el mensaje de control de IME de WM \_ \_ con la configuración de parámetros que se muestra a continuación.
ms.assetid: d2c60974-a602-4a42-8a45-870ee39df001
title: Comando IMC_GETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32b8f4414311d0727f622a1b552428cd31b0716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810406"
---
# <a name="imc_getcompositionwindow-command"></a><span data-ttu-id="d5a1d-104">\_Comando IMC GETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="d5a1d-104">IMC\_GETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="d5a1d-105">Indica a una ventana de IME que obtenga la posición de la ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="d5a1d-105">Instructs an IME window to get the position of the composition window.</span></span> <span data-ttu-id="d5a1d-106">Para enviar este comando, la aplicación usa el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="d5a1d-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="d5a1d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5a1d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5a1d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5a1d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="d5a1d-109">Establezca en IMC \_ GETCOMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="d5a1d-109">Set to IMC\_GETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="d5a1d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5a1d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d5a1d-111">Puntero a una estructura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) que contiene la posición de la ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="d5a1d-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the position of the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5a1d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5a1d-112">Return Value</span></span>

<span data-ttu-id="d5a1d-113">Devuelve 0 si se realiza correctamente, o un valor distinto de cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d5a1d-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5a1d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5a1d-114">Remarks</span></span>

<span data-ttu-id="d5a1d-115">Dado que el IME puede ajustar la posición de una ventana de composición, una aplicación utiliza este comando para obtener la posición real a fin de decidir si se debe cambiar la posición de la ventana.</span><span class="sxs-lookup"><span data-stu-id="d5a1d-115">Because the IME might adjust the position of a composition window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="d5a1d-116">La posición recuperada se encuentra en coordenadas de ventana relativas a la ventana que tiene el foco de entrada actual.</span><span class="sxs-lookup"><span data-stu-id="d5a1d-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5a1d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5a1d-117">Requirements</span></span>



| <span data-ttu-id="d5a1d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5a1d-118">Requirement</span></span> | <span data-ttu-id="d5a1d-119">Value</span><span class="sxs-lookup"><span data-stu-id="d5a1d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a1d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5a1d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d5a1d-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d5a1d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d5a1d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5a1d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d5a1d-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5a1d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d5a1d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5a1d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5a1d-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5a1d-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5a1d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5a1d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5a1d-127">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="d5a1d-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d5a1d-128">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="d5a1d-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="d5a1d-129">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="d5a1d-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> </dl>

 

 




