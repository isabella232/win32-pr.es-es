---
description: Notifica a una aplicación cuando se actualiza el estado de apertura del contexto de entrada. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: cc6fa7f4-b85a-486a-985d-53c071321bd1
title: Código de notificación de IMN_SETOPENSTATUS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3598d7415cf415de3279e016d81a6d14b767d5da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082628"
---
# <a name="imn_setopenstatus-notification-code"></a><span data-ttu-id="096e7-104">Código de notificación de SETOPENSTATUS de IMN \_</span><span class="sxs-lookup"><span data-stu-id="096e7-104">IMN\_SETOPENSTATUS notification code</span></span>

<span data-ttu-id="096e7-105">Notifica a una aplicación cuando se actualiza el estado de apertura del contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="096e7-105">Notifies an application when the open status of the input context is updated.</span></span> <span data-ttu-id="096e7-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="096e7-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETOPENSTATUS
```



## <a name="parameters"></a><span data-ttu-id="096e7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="096e7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="096e7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="096e7-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="096e7-109">Establézcalo en IMN \_ SETOPENSTATUS.</span><span class="sxs-lookup"><span data-stu-id="096e7-109">Set to IMN\_SETOPENSTATUS.</span></span>

</dd> <dt>

<span data-ttu-id="096e7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="096e7-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="096e7-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="096e7-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="096e7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="096e7-112">Return Value</span></span>

<span data-ttu-id="096e7-113">Este comando no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="096e7-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="096e7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="096e7-114">Remarks</span></span>

<span data-ttu-id="096e7-115">La aplicación puede obtener información sobre el estado abierto mediante la función [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) .</span><span class="sxs-lookup"><span data-stu-id="096e7-115">The application can get information about the open status by using the [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="096e7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="096e7-116">Requirements</span></span>



| <span data-ttu-id="096e7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="096e7-117">Requirement</span></span> | <span data-ttu-id="096e7-118">Value</span><span class="sxs-lookup"><span data-stu-id="096e7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="096e7-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="096e7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="096e7-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="096e7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="096e7-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="096e7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="096e7-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="096e7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="096e7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="096e7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="096e7-124"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="096e7-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="096e7-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="096e7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="096e7-126">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="096e7-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="096e7-127">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="096e7-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="096e7-128">**ImmGetOpenStatus**</span><span class="sxs-lookup"><span data-stu-id="096e7-128">**ImmGetOpenStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)
</dt> <dt>

[<span data-ttu-id="096e7-129">**\_notificación de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="096e7-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




