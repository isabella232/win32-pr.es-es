---
title: Mensaje de WM_RASDIALEVENT (RAS. h)
description: El sistema operativo envía un \_ mensaje de WM RASDIALEVENT a un procedimiento de ventana cuando se produce un cambio de evento de estado durante un proceso de conexión RAS.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- WM_RASDIALEVENT el mensaje RAS
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470fe3915c9f672c4663971159386e529ea60db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676565"
---
# <a name="wm_rasdialevent-message"></a><span data-ttu-id="ec513-104">Mensaje de RASDIALEVENT de WM \_</span><span class="sxs-lookup"><span data-stu-id="ec513-104">WM\_RASDIALEVENT message</span></span>

<span data-ttu-id="ec513-105">El sistema operativo envía un mensaje de **WM \_ RASDIALEVENT** a un procedimiento de ventana cuando se produce un cambio de evento de estado durante un proceso de conexión RAS.</span><span class="sxs-lookup"><span data-stu-id="ec513-105">The operating system sends a **WM\_RASDIALEVENT** message to a window procedure when a change of state event occurs during a RAS connection process.</span></span> <span data-ttu-id="ec513-106">Esto sucede cuando se ha especificado una ventana para controlar las notificaciones de estos eventos mediante el parámetro de *notificador* de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span><span class="sxs-lookup"><span data-stu-id="ec513-106">This happens when a window has been specified to handle notifications of such events by using the *notifier* parameter of [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span></span>

<span data-ttu-id="ec513-107">Los dos parámetros de mensaje son equivalentes a los parámetros de los mismos nombres que se usan con las funciones de devolución de llamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) y [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="ec513-107">The two message parameters are equivalent to the parameters of the same names that are used with [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span>


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a><span data-ttu-id="ec513-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec513-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec513-109">*rasconnstate*</span><span class="sxs-lookup"><span data-stu-id="ec513-109">*rasconnstate*</span></span> 
</dt> <dd>

<span data-ttu-id="ec513-110">Valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="ec513-110">Value of *wParam*.</span></span> <span data-ttu-id="ec513-111">Equivalente al parámetro *rasconnstate* de las funciones de devolución de llamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) y [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="ec513-111">Equivalent to the *rasconnstate* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="ec513-112">Especifica un valor de enumerador [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) que indica el estado que está a punto de entrar en el proceso de conexión de acceso remoto rasdial.</span><span class="sxs-lookup"><span data-stu-id="ec513-112">Specifies a [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumerator value that indicates the state the RasDial remote access connection process is about to enter.</span></span>

</dd> <dt>

<span data-ttu-id="ec513-113">*dwError*</span><span class="sxs-lookup"><span data-stu-id="ec513-113">*dwError*</span></span> 
</dt> <dd>

<span data-ttu-id="ec513-114">Valor de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="ec513-114">Value of *lParam*.</span></span> <span data-ttu-id="ec513-115">Equivalente al parámetro *dwError* de las funciones de devolución de llamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) y [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="ec513-115">Equivalent to the *dwError* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="ec513-116">Un valor distinto de cero indica el error que se ha producido, o cero si no se ha producido ningún error.</span><span class="sxs-lookup"><span data-stu-id="ec513-116">A nonzero value indicates the error that has occurred, or zero if no error has occurred.</span></span>

<span data-ttu-id="ec513-117">[**Rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) envía este mensaje con el valor de *dwError* establecido en cero cuando se entra en cada estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="ec513-117">[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) sends this message with *dwError* set to zero upon entry to each connection state.</span></span> <span data-ttu-id="ec513-118">Si se produce un error dentro de un estado, el mensaje se envía de nuevo para el estado, esta vez con un valor *dwError* distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="ec513-118">If an error occurs within a state, the message is sent again for the state, this time with a nonzero *dwError* value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec513-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec513-119">Return value</span></span>

<span data-ttu-id="ec513-120">Si una aplicación procesa este mensaje, debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="ec513-120">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec513-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec513-121">Requirements</span></span>



| <span data-ttu-id="ec513-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec513-122">Requirement</span></span> | <span data-ttu-id="ec513-123">Value</span><span class="sxs-lookup"><span data-stu-id="ec513-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec513-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec513-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ec513-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ec513-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ec513-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec513-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ec513-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec513-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ec513-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec513-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec513-129"><dt>Ras. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec513-129"><dt>Ras.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec513-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec513-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec513-131">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="ec513-131">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="ec513-132">Mensajes del servicio de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="ec513-132">Remote Access Service Messages</span></span>](remote-access-service-messages.md)
</dt> <dt>

[<span data-ttu-id="ec513-133">**RasDial**</span><span class="sxs-lookup"><span data-stu-id="ec513-133">**RasDial**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[<span data-ttu-id="ec513-134">**RasDialFunc**</span><span class="sxs-lookup"><span data-stu-id="ec513-134">**RasDialFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[<span data-ttu-id="ec513-135">**RasDialFunc1**</span><span class="sxs-lookup"><span data-stu-id="ec513-135">**RasDialFunc1**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

<span data-ttu-id="ec513-136">[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ec513-136">[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span></span>
</dt> </dl>

 

