---
description: Notifica a una aplicación cuando un IME está a punto de abrir la ventana candidata. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 439ff125-2731-4eb1-8287-4ca8ace7d8ec
title: Evento IMN_OPENCANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f8f412c60cc6b62904e562d450479af642de0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910110"
---
# <a name="imn_opencandidate-event"></a><span data-ttu-id="edc97-104">\_Evento imn OPENCANDIDATE</span><span class="sxs-lookup"><span data-stu-id="edc97-104">IMN\_OPENCANDIDATE event</span></span>

<span data-ttu-id="edc97-105">Notifica a una aplicación cuando un IME está a punto de abrir la ventana candidata.</span><span class="sxs-lookup"><span data-stu-id="edc97-105">Notifies an application when an IME is about to open the candidate window.</span></span> <span data-ttu-id="edc97-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="edc97-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENCANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="edc97-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edc97-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edc97-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="edc97-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="edc97-109">Establézcalo en IMN \_ OPENCANDIDATE.</span><span class="sxs-lookup"><span data-stu-id="edc97-109">Set to IMN\_OPENCANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="edc97-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="edc97-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="edc97-111">Marca de lista de candidatos.</span><span class="sxs-lookup"><span data-stu-id="edc97-111">Candidate list flag.</span></span> <span data-ttu-id="edc97-112">Cada bit corresponde a una lista de candidatos: bit 0 a la primera lista, bit 1 a segundo, etc.</span><span class="sxs-lookup"><span data-stu-id="edc97-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="edc97-113">Si un bit especificado es 1, la ventana candidata correspondiente está a punto de abrirse.</span><span class="sxs-lookup"><span data-stu-id="edc97-113">If a specified bit is 1, the corresponding candidate window is about to be opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edc97-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edc97-114">Return Value</span></span>

<span data-ttu-id="edc97-115">Este comando no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="edc97-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="edc97-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edc97-116">Remarks</span></span>

<span data-ttu-id="edc97-117">Una aplicación debe procesar este comando si muestra los propios candidatos.</span><span class="sxs-lookup"><span data-stu-id="edc97-117">An application should process this command if it displays candidates itself.</span></span> <span data-ttu-id="edc97-118">La aplicación puede recuperar una lista de candidatos para mostrar mediante la función [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) .</span><span class="sxs-lookup"><span data-stu-id="edc97-118">The application can retrieve a list of candidates to display by using the [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) function.</span></span>

<span data-ttu-id="edc97-119">De forma predeterminada, la ventana del IME crea una ventana candidata cuando procesa este comando.</span><span class="sxs-lookup"><span data-stu-id="edc97-119">By default, the IME window creates a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="edc97-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edc97-120">Requirements</span></span>



| <span data-ttu-id="edc97-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="edc97-121">Requirement</span></span> | <span data-ttu-id="edc97-122">Value</span><span class="sxs-lookup"><span data-stu-id="edc97-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edc97-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edc97-123">Minimum supported client</span></span><br/> | <span data-ttu-id="edc97-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="edc97-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="edc97-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edc97-125">Minimum supported server</span></span><br/> | <span data-ttu-id="edc97-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="edc97-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="edc97-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edc97-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="edc97-128"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edc97-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edc97-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="edc97-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edc97-130">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="edc97-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="edc97-131">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="edc97-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="edc97-132">**ImmGetCandidateList**</span><span class="sxs-lookup"><span data-stu-id="edc97-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="edc97-133">**\_notificación de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="edc97-133">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




