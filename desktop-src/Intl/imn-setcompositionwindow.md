---
description: Notifica a una aplicación cuando se actualiza el estilo o la posición de la ventana de composición. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 07a9f0f6-587e-47c6-8f18-b48bdab0a541
title: Código de notificación de IMN_SETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a1a4e989fb36049168359f86f85ee7a58103a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002780"
---
# <a name="imn_setcompositionwindow-notification-code"></a><span data-ttu-id="eea12-104">Código de notificación de SETCOMPOSITIONWINDOW de IMN \_</span><span class="sxs-lookup"><span data-stu-id="eea12-104">IMN\_SETCOMPOSITIONWINDOW notification code</span></span>

<span data-ttu-id="eea12-105">Notifica a una aplicación cuando se actualiza el estilo o la posición de la ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="eea12-105">Notifies an application when the style or position of the composition window is updated.</span></span> <span data-ttu-id="eea12-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="eea12-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="eea12-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eea12-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eea12-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="eea12-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="eea12-109">Establézcalo en IMN \_ SETCOMPOSITIONWINDOW.</span><span class="sxs-lookup"><span data-stu-id="eea12-109">Set to IMN\_SETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="eea12-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="eea12-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="eea12-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="eea12-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eea12-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eea12-112">Return Value</span></span>

<span data-ttu-id="eea12-113">Este comando no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="eea12-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eea12-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eea12-114">Remarks</span></span>

<span data-ttu-id="eea12-115">La aplicación puede obtener información sobre el formulario de composición mediante el comando [**IMC \_ GETCOMPOSITIONWINDOW**](imc-getcompositionwindow.md) .</span><span class="sxs-lookup"><span data-stu-id="eea12-115">The application can get information about the composition form by using the [**IMC\_GETCOMPOSITIONWINDOW**](imc-getcompositionwindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea12-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eea12-116">Requirements</span></span>



| <span data-ttu-id="eea12-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="eea12-117">Requirement</span></span> | <span data-ttu-id="eea12-118">Value</span><span class="sxs-lookup"><span data-stu-id="eea12-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eea12-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eea12-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eea12-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eea12-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eea12-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eea12-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eea12-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eea12-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eea12-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eea12-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eea12-124"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eea12-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eea12-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="eea12-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea12-126">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="eea12-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="eea12-127">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="eea12-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="eea12-128">**GETCOMPOSITIONWINDOW de IMC \_**</span><span class="sxs-lookup"><span data-stu-id="eea12-128">**IMC\_GETCOMPOSITIONWINDOW**</span></span>](imc-getcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="eea12-129">**\_notificación de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="eea12-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




