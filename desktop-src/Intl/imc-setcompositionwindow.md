---
description: Indica a una ventana del IME que establezca el estilo de la ventana de composición. Para enviar este comando, la aplicación usa el mensaje de control de IME de WM \_ \_ con la configuración de parámetros que se muestra a continuación.
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: Comando IMC_SETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b06c53b1ff2ec343d6382dd48d0d4108cf403c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686922"
---
# <a name="imc_setcompositionwindow-command"></a><span data-ttu-id="a05f7-104">\_Comando IMC SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="a05f7-104">IMC\_SETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="a05f7-105">Indica a una ventana del IME que establezca el estilo de la ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="a05f7-105">Instructs an IME window to set the style of the composition window.</span></span> <span data-ttu-id="a05f7-106">Para enviar este comando, la aplicación usa el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="a05f7-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="a05f7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a05f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a05f7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="a05f7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="a05f7-109">Establezca en IMC \_ SETCOMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="a05f7-109">Set to IMC\_SETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="a05f7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="a05f7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="a05f7-111">Puntero a una estructura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) que contiene la información de estilo.</span><span class="sxs-lookup"><span data-stu-id="a05f7-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the style information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a05f7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a05f7-112">Return Value</span></span>

<span data-ttu-id="a05f7-113">Devuelve 0 si se realiza correctamente, o un valor distinto de cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a05f7-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a05f7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a05f7-114">Remarks</span></span>

<span data-ttu-id="a05f7-115">Este comando establece el estilo en el contexto de entrada actual y el estilo se aplica posteriormente a cada ventana del IME que recibe ese contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="a05f7-115">This command sets the style in the current input context, and the style is subsequently applied to each IME window that receives that input context.</span></span>

<span data-ttu-id="a05f7-116">De forma predeterminada, la ventana del IME tiene el estilo de punto de CFS \_ .</span><span class="sxs-lookup"><span data-stu-id="a05f7-116">By default, the IME window has the CFS\_POINT style.</span></span> <span data-ttu-id="a05f7-117">Con este estilo, la ventana del IME usa la posición del símbolo de intercalación actual y el área de cliente de la ventana cuando abre cualquier ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="a05f7-117">With this style, the IME window uses the current caret position and window client area when it opens any composition window.</span></span>

## <a name="requirements"></a><span data-ttu-id="a05f7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a05f7-118">Requirements</span></span>



| <span data-ttu-id="a05f7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a05f7-119">Requirement</span></span> | <span data-ttu-id="a05f7-120">Value</span><span class="sxs-lookup"><span data-stu-id="a05f7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a05f7-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a05f7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a05f7-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a05f7-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a05f7-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a05f7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a05f7-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a05f7-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a05f7-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a05f7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a05f7-126"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a05f7-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a05f7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a05f7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a05f7-128">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="a05f7-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="a05f7-129">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="a05f7-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="a05f7-130">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="a05f7-130">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="a05f7-131">**\_control IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a05f7-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




