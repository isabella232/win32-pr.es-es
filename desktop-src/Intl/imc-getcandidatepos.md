---
description: Indica a una ventana del IME que obtenga la posición de la ventana candidata. Para enviar este comando, la aplicación usa el mensaje de control de IME de WM \_ \_ con la configuración de parámetros que se muestra a continuación.
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: Comando IMC_GETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb5cd143bf45f9bdb37be4cbe3078a483f53db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653111"
---
# <a name="imc_getcandidatepos-command"></a><span data-ttu-id="a86ef-104">\_Comando IMC GETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="a86ef-104">IMC\_GETCANDIDATEPOS command</span></span>

<span data-ttu-id="a86ef-105">Indica a una ventana del IME que obtenga la posición de la ventana candidata.</span><span class="sxs-lookup"><span data-stu-id="a86ef-105">Instructs an IME window to get the position of the candidate window.</span></span> <span data-ttu-id="a86ef-106">Para enviar este comando, la aplicación usa el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="a86ef-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="a86ef-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a86ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a86ef-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="a86ef-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="a86ef-109">Establezca en IMC \_ GETCANDIDATEPOS.</span><span class="sxs-lookup"><span data-stu-id="a86ef-109">Set to IMC\_GETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="a86ef-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="a86ef-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="a86ef-111">Puntero a una estructura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) que contiene la posición de la ventana candidata.</span><span class="sxs-lookup"><span data-stu-id="a86ef-111">Pointer to a [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) structure that contains the position of the candidate window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a86ef-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a86ef-112">Return Value</span></span>

<span data-ttu-id="a86ef-113">Devuelve 0 si se realiza correctamente, o un valor distinto de cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a86ef-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a86ef-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a86ef-114">Remarks</span></span>

<span data-ttu-id="a86ef-115">Dado que el IME puede ajustar la posición de una ventana candidata, una aplicación utiliza este comando para obtener la posición real a fin de decidir si se debe cambiar la posición de la ventana.</span><span class="sxs-lookup"><span data-stu-id="a86ef-115">Because the IME might adjust the position of a candidate window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="a86ef-116">La posición recuperada se encuentra en coordenadas de ventana relativas a la ventana que tiene el foco de entrada actual.</span><span class="sxs-lookup"><span data-stu-id="a86ef-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="a86ef-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a86ef-117">Requirements</span></span>



| <span data-ttu-id="a86ef-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a86ef-118">Requirement</span></span> | <span data-ttu-id="a86ef-119">Value</span><span class="sxs-lookup"><span data-stu-id="a86ef-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a86ef-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a86ef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a86ef-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a86ef-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a86ef-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a86ef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a86ef-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a86ef-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a86ef-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a86ef-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a86ef-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a86ef-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a86ef-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a86ef-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a86ef-127">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="a86ef-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="a86ef-128">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="a86ef-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="a86ef-129">**CANDIDATEFORM**</span><span class="sxs-lookup"><span data-stu-id="a86ef-129">**CANDIDATEFORM**</span></span>](/windows/win32/api/imm/ns-imm-candidateform)
</dt> </dl>

 

 




