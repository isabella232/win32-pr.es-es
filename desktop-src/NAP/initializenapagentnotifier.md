---
title: Función InitializeNapAgentNotifier (NapUtil. h)
description: Suscribe el proceso de llamada a las notificaciones de cambio de estado NapAgent y las notificaciones de cambio de estado de cuarentena.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- InitializeNapAgentNotifier función NAP
topic_type:
- apiref
api_name:
- InitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f59c4c342f693038040f374bbdbcdb8ab226f74d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996175"
---
# <a name="initializenapagentnotifier-function"></a><span data-ttu-id="3e273-104">InitializeNapAgentNotifier función)</span><span class="sxs-lookup"><span data-stu-id="3e273-104">InitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="3e273-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="3e273-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3e273-106">La función **InitializeNapAgentNotifier** suscribe el proceso de llamada a las notificaciones de cambio de estado NapAgent y notificaciones de cambio de estado de cuarentena.</span><span class="sxs-lookup"><span data-stu-id="3e273-106">The **InitializeNapAgentNotifier** function subscribes the calling process to NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="3e273-107">Estas notificaciones las proporciona el servicio NapAgent.</span><span class="sxs-lookup"><span data-stu-id="3e273-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e273-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e273-108">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a><span data-ttu-id="3e273-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e273-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e273-110">*tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3e273-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e273-111">Valor [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) que especifica el tipo de notificaciones de servicio que se van a recibir.</span><span class="sxs-lookup"><span data-stu-id="3e273-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to receive.</span></span>

</dd> <dt>

<span data-ttu-id="3e273-112">*hNotifyEvent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e273-112">*hNotifyEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e273-113">Identificador de eventos que se usa para la notificación.</span><span class="sxs-lookup"><span data-stu-id="3e273-113">An event handle used for notification.</span></span> <span data-ttu-id="3e273-114">El autor de la llamada debe pasar un identificador abierto al parámetro *hNotifyEvent* .</span><span class="sxs-lookup"><span data-stu-id="3e273-114">The caller must pass an open handle to the *hNotifyEvent* parameter.</span></span> <span data-ttu-id="3e273-115">El llamador también debe cerrar el controlador de eventos cuando ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="3e273-115">The caller must also close the event handle when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e273-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e273-116">Return value</span></span>



| <span data-ttu-id="3e273-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3e273-117">Return code</span></span>                                                                                                | <span data-ttu-id="3e273-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e273-118">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e273-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3e273-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="3e273-120">La inicialización se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e273-120">Initialization completed successfully.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="3e273-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="3e273-121"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="3e273-122">Error de inicialización.</span><span class="sxs-lookup"><span data-stu-id="3e273-122">Initialization failed.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="3e273-123"><dt>**ERROR \_ ya \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="3e273-123"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="3e273-124">El proceso ya se ha suscrito a las notificaciones de servicio de NapAgent del *tipo* especificado.</span><span class="sxs-lookup"><span data-stu-id="3e273-124">The process has already subscribed to NapAgent service notifications of the *type* specified.</span></span> <br/> |
| <dl> <span data-ttu-id="3e273-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3e273-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="3e273-126">Se pasó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="3e273-126">An invalid argument was passed.</span></span> <br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="3e273-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e273-127">Remarks</span></span>

<span data-ttu-id="3e273-128">Esta función no es segura para los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="3e273-128">This function is not thread safe.</span></span>

<span data-ttu-id="3e273-129">Cada proceso que requiere una suscripción a las notificaciones de servicio de NapAgent del *tipo* especificado debe llamar a **InitializeNapAgentNotifier** para suscribirse a las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="3e273-129">Each process that requires a subscription to NapAgent service notifications of the specified *type* must call **InitializeNapAgentNotifier** to subscribe to notifications.</span></span> <span data-ttu-id="3e273-130">Si un proceso debe suscribirse a más de un tipo de notificación, debe llamar a **InitializeNapAgentNotifier** una vez para cada tipo de notificación.</span><span class="sxs-lookup"><span data-stu-id="3e273-130">If a process must subscribe to more than one type of notification, it must call **InitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="3e273-131">Una vez que un proceso no requiere más notificaciones, el proceso debe llamar a [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) para el *tipo* especificado.</span><span class="sxs-lookup"><span data-stu-id="3e273-131">Once a process does not require further notifications, the process must call [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) for the specified *type*.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e273-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e273-132">Requirements</span></span>



| <span data-ttu-id="3e273-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e273-133">Requirement</span></span> | <span data-ttu-id="3e273-134">Value</span><span class="sxs-lookup"><span data-stu-id="3e273-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3e273-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e273-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3e273-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3e273-136">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3e273-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e273-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3e273-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e273-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3e273-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e273-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e273-140"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e273-140"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="3e273-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e273-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e273-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e273-142"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e273-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e273-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e273-144">**UninitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="3e273-144">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





