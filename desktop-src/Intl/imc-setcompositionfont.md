---
description: Indica a una ventana de IME que especifique la fuente lógica que se va a utilizar para mostrar caracteres intermedios en la ventana de composición. Para enviar este comando, la aplicación usa el mensaje de control de IME de WM \_ \_ con la configuración de parámetros que se muestra a continuación.
ms.assetid: 17b222e7-bf57-4cdd-8475-d9a8be03ab7f
title: Comando IMC_SETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb84c9e05ab19206064988a71b0ffc39b21a44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908127"
---
# <a name="imc_setcompositionfont-command"></a><span data-ttu-id="f87be-104">\_Comando IMC SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="f87be-104">IMC\_SETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="f87be-105">Indica a una ventana de IME que especifique la fuente lógica que se va a utilizar para mostrar caracteres intermedios en la ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="f87be-105">Instructs an IME window to specify the logical font to use for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="f87be-106">Para enviar este comando, la aplicación usa el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="f87be-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="f87be-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f87be-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f87be-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="f87be-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="f87be-109">Establezca en IMC \_ SETCOMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="f87be-109">Set to IMC\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="f87be-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f87be-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f87be-111">Puntero a una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contiene información sobre la fuente lógica.</span><span class="sxs-lookup"><span data-stu-id="f87be-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f87be-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f87be-112">Return Value</span></span>

<span data-ttu-id="f87be-113">Devuelve 0 si se realiza correctamente, o un valor distinto de cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f87be-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f87be-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f87be-114">Remarks</span></span>

<span data-ttu-id="f87be-115">Al procesar este comando, la ventana del IME cambia la fuente seleccionada actualmente en el contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="f87be-115">When processing this command, the IME window changes the current selected font in the input context.</span></span>

## <a name="requirements"></a><span data-ttu-id="f87be-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f87be-116">Requirements</span></span>



| <span data-ttu-id="f87be-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f87be-117">Requirement</span></span> | <span data-ttu-id="f87be-118">Value</span><span class="sxs-lookup"><span data-stu-id="f87be-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f87be-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f87be-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f87be-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f87be-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f87be-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f87be-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f87be-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f87be-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f87be-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f87be-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f87be-124"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f87be-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f87be-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f87be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f87be-126">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="f87be-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f87be-127">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="f87be-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="f87be-128">**\_control IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f87be-128">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
