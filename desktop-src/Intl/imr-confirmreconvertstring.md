---
description: Notifica a una aplicación cuando el IME debe cambiar la estructura RECONVERTSTRING. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: Código de notificación de IMR_CONFIRMRECONVERTSTRING (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c500a155be14f447bb07ad506e12d5bece66e225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813683"
---
# <a name="imr_confirmreconvertstring-notification-code"></a><span data-ttu-id="13013-104">Código de notificación de IMR \_ CONFIRMRECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="13013-104">IMR\_CONFIRMRECONVERTSTRING notification code</span></span>

<span data-ttu-id="13013-105">Notifica a una aplicación cuando el IME debe cambiar la estructura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="13013-105">Notifies an application when the IME needs to change the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="13013-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="13013-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="13013-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13013-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13013-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="13013-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="13013-109">Establezca en IMR \_ CONFIRMRECONVERTSTRING.</span><span class="sxs-lookup"><span data-stu-id="13013-109">Set to IMR\_CONFIRMRECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="13013-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="13013-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="13013-111">Puntero a una estructura de [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) desde el IME.</span><span class="sxs-lookup"><span data-stu-id="13013-111">Pointer to a [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure from the IME.</span></span> <span data-ttu-id="13013-112">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="13013-112">For more information, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13013-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13013-113">Return Value</span></span>

<span data-ttu-id="13013-114">Devuelve un valor distinto de cero si la aplicación acepta la estructura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) modificada.</span><span class="sxs-lookup"><span data-stu-id="13013-114">Returns a nonzero value if the application accepts the changed [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="13013-115">De lo contrario, el comando devuelve 0 y el IME usa la estructura **RECONVERTSTRING** original.</span><span class="sxs-lookup"><span data-stu-id="13013-115">Otherwise, the command returns 0 and the IME uses the original **RECONVERTSTRING** structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="13013-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13013-116">Remarks</span></span>

<span data-ttu-id="13013-117">La aplicación rellena la estructura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) al recibir el comando [IMR \_ RECONVERTSTRING](imr-reconvertstring.md) .</span><span class="sxs-lookup"><span data-stu-id="13013-117">The application fills in the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure upon receiving the [IMR\_RECONVERTSTRING](imr-reconvertstring.md) command.</span></span>

<span data-ttu-id="13013-118">Una vez que la aplicación ha controlado una [IMR \_ RECONVERTSTRING](imr-reconvertstring.md), el IME podría o no ajustar la estructura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="13013-118">After the application has handled [IMR\_RECONVERTSTRING](imr-reconvertstring.md), the IME might or might not adjust the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span> <span data-ttu-id="13013-119">El IME envía una \_ solicitud del IME \_ de WM con **IMR \_ CONFIRMRECONVERTSTRING** para confirmar los cambios en la estructura **RECONVERTSTRING** .</span><span class="sxs-lookup"><span data-stu-id="13013-119">The IME sends WM\_IME\_REQUEST with **IMR\_CONFIRMRECONVERTSTRING** to confirm the changes to the **RECONVERTSTRING** structure.</span></span> <span data-ttu-id="13013-120">Si la aplicación devuelve **true** para **IMR \_ CONFIRMRECONVERTSTRING**, el IME genera una nueva cadena de composición basada en la estructura **RECONVERTSTRING** para el comando **IMR \_ CONFIRMRECONVERTSTRING** .</span><span class="sxs-lookup"><span data-stu-id="13013-120">If the application returns **TRUE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the **RECONVERTSTRING** structure for the **IMR\_CONFIRMRECONVERTSTRING** command.</span></span> <span data-ttu-id="13013-121">Si la aplicación devuelve **false** para **IMR \_ CONFIRMRECONVERTSTRING**, el IME genera una nueva cadena de composición basada en la estructura **RECONVERTSTRING** original especificada por la aplicación en el \_ comando IMR RECONVERTSTRING.</span><span class="sxs-lookup"><span data-stu-id="13013-121">If the application returns **FALSE** for **IMR\_CONFIRMRECONVERTSTRING**, the IME generates a new composition string based on the original **RECONVERTSTRING** structure specified by the application in the IMR\_RECONVERTSTRING command.</span></span>

## <a name="requirements"></a><span data-ttu-id="13013-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13013-122">Requirements</span></span>



| <span data-ttu-id="13013-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="13013-123">Requirement</span></span> | <span data-ttu-id="13013-124">Value</span><span class="sxs-lookup"><span data-stu-id="13013-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13013-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13013-125">Minimum supported client</span></span><br/> | <span data-ttu-id="13013-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="13013-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="13013-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13013-127">Minimum supported server</span></span><br/> | <span data-ttu-id="13013-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13013-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="13013-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13013-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="13013-130"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13013-130"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13013-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="13013-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13013-132">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="13013-132">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="13013-133">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="13013-133">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="13013-134">IMR \_ RECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="13013-134">IMR\_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> <dt>

[<span data-ttu-id="13013-135">**RECONVERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="13013-135">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="13013-136">**\_solicitud de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="13013-136">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




