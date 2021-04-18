---
description: Notifica a una aplicación cuando ha finalizado el procesamiento del candidato y el IME está a punto de quitar la ventana candidata. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: Código de notificación de IMN_SETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03171a76ce94572d2425f8e75f1cbe45b7efe4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652705"
---
# <a name="imn_setcandidatepos-notification-code"></a><span data-ttu-id="a408a-104">Código de notificación de SETCANDIDATEPOS de IMN \_</span><span class="sxs-lookup"><span data-stu-id="a408a-104">IMN\_SETCANDIDATEPOS notification code</span></span>

<span data-ttu-id="a408a-105">Notifica a una aplicación cuando ha finalizado el procesamiento del candidato y el IME está a punto de quitar la ventana candidata.</span><span class="sxs-lookup"><span data-stu-id="a408a-105">Notifies an application when candidate processing has finished and the IME is about to move the candidate window.</span></span> <span data-ttu-id="a408a-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="a408a-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a><span data-ttu-id="a408a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a408a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a408a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="a408a-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="a408a-109">Establézcalo en IMN \_ SETCANDIDATEPOS.</span><span class="sxs-lookup"><span data-stu-id="a408a-109">Set to IMN\_SETCANDIDATEPOS.</span></span>

</dd> <dt>

<span data-ttu-id="a408a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="a408a-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="a408a-111">Marca de lista de candidatos.</span><span class="sxs-lookup"><span data-stu-id="a408a-111">Candidate list flag.</span></span> <span data-ttu-id="a408a-112">Cada bit corresponde a una lista de candidatos: bit 0 a la primera lista, bit 1 a segundo, etc.</span><span class="sxs-lookup"><span data-stu-id="a408a-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="a408a-113">Si un bit especificado es 1, la ventana candidata correspondiente está a punto de moverse.</span><span class="sxs-lookup"><span data-stu-id="a408a-113">If a specified bit is 1, the corresponding candidate window is about to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a408a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a408a-114">Return Value</span></span>

<span data-ttu-id="a408a-115">Este comando no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="a408a-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a408a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a408a-116">Remarks</span></span>

<span data-ttu-id="a408a-117">Una aplicación debe procesar este comando si muestra la ventana de candidato.</span><span class="sxs-lookup"><span data-stu-id="a408a-117">An application should process this command if it displays the candidate window itself.</span></span>

<span data-ttu-id="a408a-118">La ventana del IME mueve la ventana candidata cuando procesa este comando.</span><span class="sxs-lookup"><span data-stu-id="a408a-118">The IME window moves the candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="a408a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a408a-119">Requirements</span></span>



| <span data-ttu-id="a408a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a408a-120">Requirement</span></span> | <span data-ttu-id="a408a-121">Value</span><span class="sxs-lookup"><span data-stu-id="a408a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a408a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a408a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a408a-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a408a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a408a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a408a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a408a-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a408a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a408a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a408a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a408a-127"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a408a-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a408a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a408a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a408a-129">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="a408a-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="a408a-130">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="a408a-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="a408a-131">**\_notificación de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a408a-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




