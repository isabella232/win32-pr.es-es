---
description: Notifica a una aplicación cuando se actualiza el modo de conversión del contexto de entrada. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 62bb9717-cc41-4e34-af1a-ff41324bd3a9
title: Código de notificación de IMN_SETCONVERSIONMODE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c0ba945b9988ddb32d86c2005ec240c16f82ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688337"
---
# <a name="imn_setconversionmode-notification-code"></a><span data-ttu-id="2bc5c-104">Código de notificación de SETCONVERSIONMODE de IMN \_</span><span class="sxs-lookup"><span data-stu-id="2bc5c-104">IMN\_SETCONVERSIONMODE notification code</span></span>

<span data-ttu-id="2bc5c-105">Notifica a una aplicación cuando se actualiza el modo de conversión del contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="2bc5c-105">Notifies an application when the conversion mode of the input context is updated.</span></span> <span data-ttu-id="2bc5c-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="2bc5c-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCONVERSIONMODE
```



## <a name="parameters"></a><span data-ttu-id="2bc5c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bc5c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bc5c-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="2bc5c-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="2bc5c-109">Establézcalo en IMN \_ SETCONVERSIONMODE.</span><span class="sxs-lookup"><span data-stu-id="2bc5c-109">Set to IMN\_SETCONVERSIONMODE.</span></span>

</dd> <dt>

<span data-ttu-id="2bc5c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="2bc5c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2bc5c-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2bc5c-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bc5c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bc5c-112">Return Value</span></span>

<span data-ttu-id="2bc5c-113">Este comando no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="2bc5c-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bc5c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bc5c-114">Remarks</span></span>

<span data-ttu-id="2bc5c-115">La aplicación puede obtener información sobre el modo de conversión mediante la función [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="2bc5c-115">The application can get information about the conversion mode by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bc5c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bc5c-116">Requirements</span></span>



| <span data-ttu-id="2bc5c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bc5c-117">Requirement</span></span> | <span data-ttu-id="2bc5c-118">Value</span><span class="sxs-lookup"><span data-stu-id="2bc5c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc5c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bc5c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2bc5c-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2bc5c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2bc5c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bc5c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2bc5c-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2bc5c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2bc5c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bc5c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bc5c-124"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2bc5c-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bc5c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bc5c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc5c-126">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="2bc5c-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="2bc5c-127">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="2bc5c-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="2bc5c-128">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="2bc5c-128">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="2bc5c-129">**\_notificación de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="2bc5c-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




