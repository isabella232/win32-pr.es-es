---
description: Notifica a una aplicación cuando un IME seleccionado necesita una cadena para la reconversión. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: Código de notificación de IMR_RECONVERTSTRING (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbb1caeedb729b176f116a15e64879d79d519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909501"
---
# <a name="imr_reconvertstring-notification-code"></a><span data-ttu-id="d1951-104">Código de notificación de IMR \_ RECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="d1951-104">IMR\_RECONVERTSTRING notification code</span></span>

<span data-ttu-id="d1951-105">Notifica a una aplicación cuando un IME seleccionado necesita una cadena para la reconversión.</span><span class="sxs-lookup"><span data-stu-id="d1951-105">Notifies an application when a selected IME needs a string for reconversion.</span></span> <span data-ttu-id="d1951-106">La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con la configuración de parámetros, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="d1951-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a><span data-ttu-id="d1951-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1951-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1951-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1951-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="d1951-109">Establezca en IMR \_ RECONVERTSTRING.</span><span class="sxs-lookup"><span data-stu-id="d1951-109">Set to IMR\_RECONVERTSTRING.</span></span>

</dd> <dt>

<span data-ttu-id="d1951-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1951-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d1951-111">Puntero a un búfer que contiene la estructura y las cadenas de [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="d1951-111">Pointer to a buffer containing the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure and strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1951-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1951-112">Return Value</span></span>

<span data-ttu-id="d1951-113">Devuelve la estructura de la cadena de reconversión actual.</span><span class="sxs-lookup"><span data-stu-id="d1951-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="d1951-114">Si *lParam* se establece en **null**, la aplicación devuelve el tamaño del búfer necesario para contener la estructura.</span><span class="sxs-lookup"><span data-stu-id="d1951-114">If *lParam* is set to **NULL**, the application returns the size for the buffer required to hold the structure.</span></span> <span data-ttu-id="d1951-115">El comando devuelve 0 si no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="d1951-115">The command returns 0 if it does not succeed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1951-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1951-116">Requirements</span></span>



| <span data-ttu-id="d1951-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1951-117">Requirement</span></span> | <span data-ttu-id="d1951-118">Value</span><span class="sxs-lookup"><span data-stu-id="d1951-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1951-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1951-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d1951-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d1951-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d1951-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1951-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d1951-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d1951-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d1951-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1951-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1951-124"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1951-124"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1951-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1951-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1951-126">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="d1951-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d1951-127">Comandos del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="d1951-127">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="d1951-128">**RECONVERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="d1951-128">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="d1951-129">**\_solicitud de IME de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d1951-129">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




