---
description: Notifica a la aplicación cuando un IME está a punto de cambiar el contenido de la ventana candidata. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: Código de notificación de IMN_CHANGECANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197380c3cf6369e0dbfd7dbca76bb3b84334eb6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156585"
---
# <a name="imn_changecandidate-notification-code"></a><span data-ttu-id="688d9-104">Código de notificación de CHANGECANDIDATE de IMN \_</span><span class="sxs-lookup"><span data-stu-id="688d9-104">IMN\_CHANGECANDIDATE notification code</span></span>

<span data-ttu-id="688d9-105">Notifica a la aplicación cuando un IME está a punto de cambiar el contenido de la ventana candidata.</span><span class="sxs-lookup"><span data-stu-id="688d9-105">Notifies the application when an IME is about to change the content of the candidate window.</span></span> <span data-ttu-id="688d9-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="688d9-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="688d9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="688d9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="688d9-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="688d9-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="688d9-109">Establézcalo en IMN \_ CHANGECANDIDATE.</span><span class="sxs-lookup"><span data-stu-id="688d9-109">Set to IMN\_CHANGECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="688d9-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="688d9-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="688d9-111">Marca de lista de candidatos.</span><span class="sxs-lookup"><span data-stu-id="688d9-111">Candidate list flag.</span></span> <span data-ttu-id="688d9-112">Cada bit corresponde a una lista de candidatos: bit 0 a la primera lista, bit 1 a la segunda lista, etc.</span><span class="sxs-lookup"><span data-stu-id="688d9-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second list, and so on.</span></span> <span data-ttu-id="688d9-113">Si un bit especificado es 1, la ventana candidata correspondiente se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="688d9-113">If a specified bit is 1, the corresponding candidate window is about to be changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="688d9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="688d9-114">Return Value</span></span>

<span data-ttu-id="688d9-115">Este comando no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="688d9-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="688d9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="688d9-116">Remarks</span></span>

<span data-ttu-id="688d9-117">Una aplicación debe procesar este comando si muestra los propios candidatos.</span><span class="sxs-lookup"><span data-stu-id="688d9-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="688d9-118">La ventana del IME cambia el aspecto de la ventana candidata al procesar este comando.</span><span class="sxs-lookup"><span data-stu-id="688d9-118">The IME window changes the appearance of the candidate window when it processes this command.</span></span> <span data-ttu-id="688d9-119">Una aplicación puede obtener información sobre la ventana del sistema con [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) y [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)</span><span class="sxs-lookup"><span data-stu-id="688d9-119">An application can get information about the system window with the [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) and [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)</span></span>

## <a name="requirements"></a><span data-ttu-id="688d9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="688d9-120">Requirements</span></span>



| <span data-ttu-id="688d9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="688d9-121">Requirement</span></span> | <span data-ttu-id="688d9-122">Value</span><span class="sxs-lookup"><span data-stu-id="688d9-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="688d9-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="688d9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="688d9-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="688d9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="688d9-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="688d9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="688d9-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="688d9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="688d9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="688d9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="688d9-128"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="688d9-128"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="688d9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="688d9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="688d9-130">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="688d9-130">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="688d9-131">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="688d9-131">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="688d9-132">**ImmGetCandidateList**</span><span class="sxs-lookup"><span data-stu-id="688d9-132">**ImmGetCandidateList**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[<span data-ttu-id="688d9-133">**ImmGetCandidateListCount**</span><span class="sxs-lookup"><span data-stu-id="688d9-133">**ImmGetCandidateListCount**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[<span data-ttu-id="688d9-134">**\_notificación de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="688d9-134">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




