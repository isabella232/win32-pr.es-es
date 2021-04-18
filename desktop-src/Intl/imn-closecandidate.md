---
description: Notifica a una aplicación cuando un IME está a punto de cerrar la ventana candidatos. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b
title: Código de notificación de IMN_CLOSECANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3414d2aa37a50b7f35f0dfb936b641b7c86a932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687618"
---
# <a name="imn_closecandidate-notification-code"></a><span data-ttu-id="e7d11-104">Código de notificación de CLOSECANDIDATE de IMN \_</span><span class="sxs-lookup"><span data-stu-id="e7d11-104">IMN\_CLOSECANDIDATE notification code</span></span>

<span data-ttu-id="e7d11-105">Notifica a una aplicación cuando un IME está a punto de cerrar la ventana candidatos.</span><span class="sxs-lookup"><span data-stu-id="e7d11-105">Notifies an application when an IME is about to close the candidates window.</span></span> <span data-ttu-id="e7d11-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="e7d11-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSECANDIDATE
```



## <a name="parameters"></a><span data-ttu-id="e7d11-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7d11-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7d11-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7d11-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="e7d11-109">Establézcalo en IMN \_ CLOSECANDIDATE.</span><span class="sxs-lookup"><span data-stu-id="e7d11-109">Set to IMN\_CLOSECANDIDATE.</span></span>

</dd> <dt>

<span data-ttu-id="e7d11-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7d11-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e7d11-111">Marca de lista de candidatos.</span><span class="sxs-lookup"><span data-stu-id="e7d11-111">Candidate list flag.</span></span> <span data-ttu-id="e7d11-112">Cada bit corresponde a una lista de candidatos: bit 0 a la primera lista, bit 1 a segundo, etc.</span><span class="sxs-lookup"><span data-stu-id="e7d11-112">Each bit corresponds to a candidate list: bit 0 to the first list, bit 1 to the second, and so on.</span></span> <span data-ttu-id="e7d11-113">Si un bit especificado es 1, la ventana candidata correspondiente está a punto de cerrarse.</span><span class="sxs-lookup"><span data-stu-id="e7d11-113">If a specified bit is 1, the corresponding candidates window is about to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7d11-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7d11-114">Return Value</span></span>

<span data-ttu-id="e7d11-115">Este comando no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e7d11-115">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7d11-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7d11-116">Remarks</span></span>

<span data-ttu-id="e7d11-117">Una aplicación debe procesar este comando si muestra los propios candidatos.</span><span class="sxs-lookup"><span data-stu-id="e7d11-117">An application should process this command if it displays candidates itself.</span></span>

<span data-ttu-id="e7d11-118">De forma predeterminada, la ventana del IME destruye una ventana candidata al procesar este comando.</span><span class="sxs-lookup"><span data-stu-id="e7d11-118">By default, the IME window destroys a candidate window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d11-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7d11-119">Requirements</span></span>



| <span data-ttu-id="e7d11-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7d11-120">Requirement</span></span> | <span data-ttu-id="e7d11-121">Value</span><span class="sxs-lookup"><span data-stu-id="e7d11-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d11-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7d11-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e7d11-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e7d11-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e7d11-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7d11-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e7d11-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e7d11-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e7d11-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7d11-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7d11-127"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7d11-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7d11-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7d11-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7d11-129">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="e7d11-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e7d11-130">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="e7d11-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="e7d11-131">**\_notificación de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e7d11-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




