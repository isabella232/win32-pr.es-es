---
description: Notifica a una aplicación cuando se actualiza la posición de la ventana de estado en el contexto de entrada. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros como se indica a continuación.
ms.assetid: 15e65aff-67d9-4d1a-a6a7-b921cecb3aec
title: Código de notificación de IMN_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d76a962e9cc509a6f9ffaac900b761b868f960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687459"
---
# <a name="imn_setstatuswindowpos-notification-code"></a><span data-ttu-id="3834e-104">Código de notificación de SETSTATUSWINDOWPOS de IMN \_</span><span class="sxs-lookup"><span data-stu-id="3834e-104">IMN\_SETSTATUSWINDOWPOS notification code</span></span>

<span data-ttu-id="3834e-105">Notifica a una aplicación cuando se actualiza la posición de la ventana de estado en el contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="3834e-105">Notifies an application when the status window position in the input context is updated.</span></span> <span data-ttu-id="3834e-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="3834e-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as follows.</span></span>


```C++
IMN_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="3834e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3834e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3834e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="3834e-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="3834e-109">Establézcalo en IMN \_ SETSTATUSWINDOWPOS.</span><span class="sxs-lookup"><span data-stu-id="3834e-109">Set to IMN\_SETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="3834e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="3834e-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="3834e-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3834e-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3834e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3834e-112">Return Value</span></span>

<span data-ttu-id="3834e-113">Este comando no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="3834e-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3834e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3834e-114">Remarks</span></span>

<span data-ttu-id="3834e-115">La aplicación puede obtener información sobre la posición de la ventana de estado mediante el comando [**IMC \_ GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md) .</span><span class="sxs-lookup"><span data-stu-id="3834e-115">The application can get information about the status window position by using the [**IMC\_GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="3834e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3834e-116">Requirements</span></span>



| <span data-ttu-id="3834e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3834e-117">Requirement</span></span> | <span data-ttu-id="3834e-118">Value</span><span class="sxs-lookup"><span data-stu-id="3834e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3834e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3834e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3834e-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3834e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3834e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3834e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3834e-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3834e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3834e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3834e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3834e-124"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3834e-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3834e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3834e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3834e-126">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="3834e-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="3834e-127">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="3834e-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="3834e-128">**GETSTATUSWINDOWPOS de IMC \_**</span><span class="sxs-lookup"><span data-stu-id="3834e-128">**IMC\_GETSTATUSWINDOWPOS**</span></span>](imc-getstatuswindowpos.md)
</dt> <dt>

[<span data-ttu-id="3834e-129">**\_notificación de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="3834e-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




