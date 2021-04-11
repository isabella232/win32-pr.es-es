---
description: Indica a una ventana de IME que recupere la fuente lógica usada para mostrar caracteres intermedios en la ventana de composición. Para enviar este comando, la aplicación usa el mensaje de control de IME de WM \_ \_ con la configuración de parámetros que se muestra a continuación.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: Comando IMC_GETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696d9809cadbe4f2c0e632719401e882777888dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275568"
---
# <a name="imc_getcompositionfont-command"></a><span data-ttu-id="f7f2b-104">\_Comando IMC GETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="f7f2b-104">IMC\_GETCOMPOSITIONFONT command</span></span>

<span data-ttu-id="f7f2b-105">Indica a una ventana de IME que recupere la fuente lógica usada para mostrar caracteres intermedios en la ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-105">Instructs an IME window to retrieve the logical font used for displaying intermediate characters in the composition window.</span></span> <span data-ttu-id="f7f2b-106">Para enviar este comando, la aplicación usa el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="f7f2b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7f2b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7f2b-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7f2b-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="f7f2b-109">Establezca en IMC \_ GETCOMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-109">Set to IMC\_GETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="f7f2b-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7f2b-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f7f2b-111">Puntero a una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que recibe información sobre la fuente lógica.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-111">Pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that receives information about the logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7f2b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7f2b-112">Return Value</span></span>

<span data-ttu-id="f7f2b-113">Devuelve 0 si se realiza correctamente, o un valor distinto de cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7f2b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7f2b-114">Requirements</span></span>



| <span data-ttu-id="f7f2b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7f2b-115">Requirement</span></span> | <span data-ttu-id="f7f2b-116">Value</span><span class="sxs-lookup"><span data-stu-id="f7f2b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f2b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7f2b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f7f2b-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f7f2b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f7f2b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7f2b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f7f2b-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f7f2b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f7f2b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7f2b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7f2b-122"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7f2b-122"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7f2b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7f2b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7f2b-124">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="f7f2b-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f7f2b-125">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="f7f2b-125">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 
