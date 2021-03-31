---
description: Notifica a una aplicación cuando un IME está a punto de mostrar un mensaje de error u otra información. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: b898283a-af1a-484f-bfb8-e5d5c0ac8ee1
title: Código de notificación de IMN_GUIDELINE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4efc222f7bfceadecce0f14573cab66471b119d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360752"
---
# <a name="imn_guideline-notification-code"></a><span data-ttu-id="bb308-104">Código de notificación de instrucciones de IMN \_</span><span class="sxs-lookup"><span data-stu-id="bb308-104">IMN\_GUIDELINE notification code</span></span>

<span data-ttu-id="bb308-105">Notifica a una aplicación cuando un IME está a punto de mostrar un mensaje de error u otra información.</span><span class="sxs-lookup"><span data-stu-id="bb308-105">Notifies an application when an IME is about to show an error message or other information.</span></span> <span data-ttu-id="bb308-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="bb308-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_GUIDELINE
```



## <a name="parameters"></a><span data-ttu-id="bb308-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb308-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb308-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb308-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="bb308-109">Establezca en la \_ instrucción imn.</span><span class="sxs-lookup"><span data-stu-id="bb308-109">Set to IMN\_GUIDELINE.</span></span>

</dd> <dt>

<span data-ttu-id="bb308-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb308-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="bb308-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bb308-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb308-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb308-112">Return Value</span></span>

<span data-ttu-id="bb308-113">Este comando no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="bb308-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb308-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb308-114">Remarks</span></span>

<span data-ttu-id="bb308-115">Una aplicación procesa este comando mediante una llamada a la función [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) para recuperar el mensaje de error o la información del IME.</span><span class="sxs-lookup"><span data-stu-id="bb308-115">An application processes this command by calling the [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) function to retrieve the error message or information from the IME.</span></span>

<span data-ttu-id="bb308-116">La ventana del IME muestra el mensaje de error o la cadena de información en una ventana de información.</span><span class="sxs-lookup"><span data-stu-id="bb308-116">The IME window displays the error message or information string in an information window.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb308-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb308-117">Requirements</span></span>



| <span data-ttu-id="bb308-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb308-118">Requirement</span></span> | <span data-ttu-id="bb308-119">Value</span><span class="sxs-lookup"><span data-stu-id="bb308-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb308-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb308-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bb308-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bb308-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bb308-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb308-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bb308-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb308-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bb308-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb308-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb308-125"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb308-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb308-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb308-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb308-127">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="bb308-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="bb308-128">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="bb308-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="bb308-129">**ImmGetGuideLine**</span><span class="sxs-lookup"><span data-stu-id="bb308-129">**ImmGetGuideLine**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)
</dt> <dt>

[<span data-ttu-id="bb308-130">**\_notificación de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="bb308-130">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




