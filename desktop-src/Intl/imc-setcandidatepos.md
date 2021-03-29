---
description: Indica a una ventana del IME que establezca la posición de la ventana candidatos. Para enviar este comando, la aplicación usa el mensaje de control de IME de WM \_ \_ con la configuración de parámetros que se muestra a continuación.
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: Comando IMC_SETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ac05890e4c720c5b671faa7f20a68a96b24a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810411"
---
# <a name="imc_setcandidatepos-command"></a><span data-ttu-id="a2622-104">\_Comando IMC SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="a2622-104">IMC\_SETCANDIDATEPOS command</span></span>

<span data-ttu-id="a2622-105">Indica a una ventana del IME que establezca la posición de la ventana candidatos.</span><span class="sxs-lookup"><span data-stu-id="a2622-105">Instructs an IME window to set the position of the candidates window.</span></span> <span data-ttu-id="a2622-106">Para enviar este comando, la aplicación usa el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="a2622-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="a2622-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2622-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2622-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2622-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="a2622-109">Establezca en IMC \_ SETCANDIDATEPOS.</span><span class="sxs-lookup"><span data-stu-id="a2622-109">Set to IMC\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="a2622-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2622-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="a2622-111">Puntero a una estructura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) que contiene la coordenada x y la coordenada y de la ventana candidatos.</span><span class="sxs-lookup"><span data-stu-id="a2622-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the x coordinate and y coordinate for the candidates window.</span></span> <span data-ttu-id="a2622-112">La aplicación debe establecer el miembro **dwIndex** de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="a2622-112">The application should set the **dwIndex** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2622-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2622-113">Return Value</span></span>

<span data-ttu-id="a2622-114">Devuelve 0 si se realiza correctamente, o un valor distinto de cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a2622-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2622-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2622-115">Remarks</span></span>

<span data-ttu-id="a2622-116">Este comando está diseñado para aplicaciones que muestran los caracteres de composición por sí mismos, pero utilizan la ventana del IME para mostrar candidatos.</span><span class="sxs-lookup"><span data-stu-id="a2622-116">This command is intended for applications that display composition characters on their own but use the IME window to display candidates.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2622-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2622-117">Requirements</span></span>



| <span data-ttu-id="a2622-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2622-118">Requirement</span></span> | <span data-ttu-id="a2622-119">Value</span><span class="sxs-lookup"><span data-stu-id="a2622-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2622-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2622-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a2622-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a2622-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a2622-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2622-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a2622-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2622-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a2622-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2622-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2622-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2622-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2622-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2622-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2622-127">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="a2622-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="a2622-128">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="a2622-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="a2622-129">**CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="a2622-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[<span data-ttu-id="a2622-130">**\_control IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a2622-130">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




