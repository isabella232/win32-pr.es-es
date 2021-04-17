---
description: Notifica a una aplicación cuando se actualiza la fuente del contexto de entrada. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 946bee83-91af-4647-9b22-96d42466352c
title: Código de notificación de IMN_SETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8373954e80e420004b347bf1b40021c86ddbb876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688338"
---
# <a name="imn_setcompositionfont-notification-code"></a><span data-ttu-id="87781-104">Código de notificación de SETCOMPOSITIONFONT de IMN \_</span><span class="sxs-lookup"><span data-stu-id="87781-104">IMN\_SETCOMPOSITIONFONT notification code</span></span>

<span data-ttu-id="87781-105">Notifica a una aplicación cuando se actualiza la fuente del contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="87781-105">Notifies an application when the font of the input context is updated.</span></span> <span data-ttu-id="87781-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="87781-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCOMPOSITIONFONT
```



## <a name="parameters"></a><span data-ttu-id="87781-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87781-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87781-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="87781-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="87781-109">Establézcalo en IMN \_ SETCOMPOSITIONFONT.</span><span class="sxs-lookup"><span data-stu-id="87781-109">Set to IMN\_SETCOMPOSITIONFONT.</span></span>

</dd> <dt>

<span data-ttu-id="87781-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="87781-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="87781-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="87781-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87781-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87781-112">Return Value</span></span>

<span data-ttu-id="87781-113">Este comando no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="87781-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87781-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87781-114">Remarks</span></span>

<span data-ttu-id="87781-115">La aplicación puede obtener información sobre la fuente mediante la función [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) .</span><span class="sxs-lookup"><span data-stu-id="87781-115">The application can get information about the font by using the [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) function.</span></span> <span data-ttu-id="87781-116">La ventana IME usa posteriormente la fuente para dibujar la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="87781-116">The IME window subsequently uses the font to draw the composition string.</span></span>

## <a name="requirements"></a><span data-ttu-id="87781-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87781-117">Requirements</span></span>



| <span data-ttu-id="87781-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="87781-118">Requirement</span></span> | <span data-ttu-id="87781-119">Value</span><span class="sxs-lookup"><span data-stu-id="87781-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87781-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87781-120">Minimum supported client</span></span><br/> | <span data-ttu-id="87781-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="87781-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="87781-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87781-122">Minimum supported server</span></span><br/> | <span data-ttu-id="87781-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="87781-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="87781-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87781-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="87781-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87781-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87781-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="87781-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87781-127">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="87781-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="87781-128">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="87781-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="87781-129">**ImmGetCompositionFont**</span><span class="sxs-lookup"><span data-stu-id="87781-129">**ImmGetCompositionFont**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)
</dt> <dt>

[<span data-ttu-id="87781-130">**\_notificación de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="87781-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




