---
description: Se suscribe a las notificaciones de cambio de estado del servicio mediante una función de devolución de llamada.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: Función SubscribeServiceChangeNotifications (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: e327a44d613b514123862b1ddcb1bf302fea63ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668186"
---
# <a name="subscribeservicechangenotifications-function"></a><span data-ttu-id="4f1fc-103">SubscribeServiceChangeNotifications función)</span><span class="sxs-lookup"><span data-stu-id="4f1fc-103">SubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="4f1fc-104">Se suscribe a las notificaciones de cambio de estado del servicio mediante una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-104">Subscribes for service status change notifications using a callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f1fc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f1fc-105">Syntax</span></span>


```C++
DWORD WINAPI SubscribeServiceChangeNotifications(
  _In_     SC_HANDLE                     hService,
  _In_     SC_EVENT_TYPE                 eEventType,
  _In_     PSC_NOTIFICATION_CALLBACK     pCallback,
  _In_opt_ PVOID                         pCallbackContext,
  _Out_    PSC_NOTIFICATION_REGISTRATION *pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="4f1fc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f1fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f1fc-107">*hService* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f1fc-107">*hService* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f1fc-108">Identificador del servicio o identificador del administrador de control de servicios (SCM) para supervisar los cambios.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-108">A handle to the service or a handle to the service control manager (SCM) to monitor for changes.</span></span>

<span data-ttu-id="4f1fc-109">Los identificadores de los servicios son devueltos por la función [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) y [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y deben tener el derecho de acceso de **Estado de \_ consulta \_ de servicio** .</span><span class="sxs-lookup"><span data-stu-id="4f1fc-109">Handles to services are returned by the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) and [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function and must have the **SERVICE\_QUERY\_STATUS** access right.</span></span> <span data-ttu-id="4f1fc-110">Los identificadores del administrador de control de servicios los devuelve la función [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) y deben tener el derecho de enumerar de acceso de **\_ \_ \_ servicio SC Manager** .</span><span class="sxs-lookup"><span data-stu-id="4f1fc-110">Handles to the service control manager are returned by the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function and must have the **SC\_MANAGER\_ENUMERATE\_SERVICE** access right.</span></span>

</dd> <dt>

<span data-ttu-id="4f1fc-111">*eEventType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f1fc-111">*eEventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f1fc-112">Especifica el tipo de cambios de estado que se deben informar.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-112">Specifies the type of status changes that should be reported.</span></span> <span data-ttu-id="4f1fc-113">Este parámetro se establece en uno de los valores especificados en el [**\_ \_ tipo de evento SC**](sc-event-type.md).</span><span class="sxs-lookup"><span data-stu-id="4f1fc-113">This parameter is set to one of the values specified in [**SC\_EVENT\_TYPE**](sc-event-type.md).</span></span> <span data-ttu-id="4f1fc-114">El comportamiento de esta función es diferente en función del tipo de evento que se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-114">The behavior for this function is different depending on the event type as follows.</span></span>



| <span data-ttu-id="4f1fc-115">Value</span><span class="sxs-lookup"><span data-stu-id="4f1fc-115">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="4f1fc-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4f1fc-116">Meaning</span></span>                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <span data-ttu-id="4f1fc-117"><dt>**SC \_ \_ \_ Cambio de base de datos de eventos**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4f1fc-117"><dt>**SC\_EVENT\_DATABASE\_CHANGE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="4f1fc-118">Se ha agregado o eliminado un servicio.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-118">A service has been added or deleted.</span></span> <span data-ttu-id="4f1fc-119">El parámetro *hService* debe ser un identificador del SCM.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-119">The *hService* parameter must be a handle to the SCM.</span></span><br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <span data-ttu-id="4f1fc-120"><dt>**SC \_ \_ \_ Cambio de propiedad de evento**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4f1fc-120"><dt>**SC\_EVENT\_PROPERTY\_CHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="4f1fc-121">Se han actualizado una o varias propiedades de servicio.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-121">One or more service properties have been updated.</span></span> <span data-ttu-id="4f1fc-122">El parámetro *hService* debe ser un identificador del servicio.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-122">The *hService* parameter must be a handle to the service.</span></span><br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <span data-ttu-id="4f1fc-123"><dt>**SC \_ \_ \_ Cambio de estado de evento**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4f1fc-123"><dt>**SC\_EVENT\_STATUS\_CHANGE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="4f1fc-124">El estado de un servicio ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-124">The status of a service has changed.</span></span> <span data-ttu-id="4f1fc-125">El parámetro *hService* debe ser un identificador del servicio.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-125">The *hService* parameter must be a handle to the service.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="4f1fc-126">*pCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f1fc-126">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f1fc-127">Especifica la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-127">Specifies the callback function.</span></span> <span data-ttu-id="4f1fc-128">La devolución de llamada debe definirse como un tipo **de \_ devolución de \_ llamada de notificación SC**.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-128">The callback must be defined as having a type of **SC\_NOTIFICATION\_CALLBACK**.</span></span> <span data-ttu-id="4f1fc-129">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-129">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4f1fc-130">*pCallbackContext* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f1fc-130">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f1fc-131">Un puntero que representa el contexto para esta devolución de llamada de notificación.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-131">A pointer representing the context for this notification callback.</span></span>

</dd> <dt>

<span data-ttu-id="4f1fc-132">*pSubscription* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4f1fc-132">*pSubscription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f1fc-133">Devuelve un puntero a la suscripción resultante del registro de devolución de llamada de notificación.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-133">Returns a pointer to the subscription resulting from the notification callback registration.</span></span> <span data-ttu-id="4f1fc-134">El autor de la llamada es responsable de llamar a [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) para dejar de recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-134">The caller is responsible for calling [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) to stop receiving notifications.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f1fc-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f1fc-135">Return value</span></span>

<span data-ttu-id="4f1fc-136">Si la función se ejecuta correctamente, el valor devuelto es **error \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-136">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="4f1fc-137">Si se produce un error en la función, el valor devuelto es uno de los [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="4f1fc-137">If the function fails, the return value is one of the [system error codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="remarks"></a><span data-ttu-id="4f1fc-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f1fc-138">Remarks</span></span>

<span data-ttu-id="4f1fc-139">La función de devolución de llamada se declara como sigue:</span><span class="sxs-lookup"><span data-stu-id="4f1fc-139">The callback function is declared as follows:</span></span>


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



<span data-ttu-id="4f1fc-140">La función de devolución de llamada recibe un puntero al contexto proporcionado por el llamador.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-140">The callback function receives a pointer to the context provided by the caller.</span></span> <span data-ttu-id="4f1fc-141">La devolución de llamada se invoca como resultado del evento de cambio de estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-141">The callback is invoked as a result of the service status change event.</span></span> <span data-ttu-id="4f1fc-142">Cuando se invoca la devolución de llamada, se proporciona con un valor de máscara de la **notificación de servicio \_ \_ \* XXX**\* que indica el tipo de cambio de estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-142">When the callback is invoked, it is provided with a bitmask of **SERVICE\_NOTIFY\_\*XXX**\* values that indicating the type of service status change.</span></span> <span data-ttu-id="4f1fc-143">Cuando la devolución de llamada se proporciona con cero en lugar de un valor válido de \*\*notificación de servicio \_ \_ \* XXX\*\*\*, la aplicación debe comprobar lo que se ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-143">When the callback is provided with zero instead of a valid **SERVICE\_NOTIFY\_\*XXX**\* value, the application must verify what was changed.</span></span>

<span data-ttu-id="4f1fc-144">La función de devolución de llamada no debe bloquear la ejecución.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-144">The callback function must not block execution.</span></span> <span data-ttu-id="4f1fc-145">Si espera que la ejecución de la función de devolución de llamada tarde tiempo, descargue el trabajo que realiza en la función de devolución de llamada en un subproceso independiente mediante la puesta en cola de un elemento de trabajo en un subproceso de un grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-145">If you expect the execution of the callback function to take time, offload the work that you perform in the callback function to a separate thread by queuing a work item to a thread in a thread pool.</span></span> <span data-ttu-id="4f1fc-146">Algunos tipos de trabajo que pueden hacer que la función de devolución de llamada tarden tiempo incluyen realizar e/s de archivos, esperar en un evento y realizar llamadas a procedimientos remotos externos.</span><span class="sxs-lookup"><span data-stu-id="4f1fc-146">Some types of work that can make the callback function take time include performing file I/O, waiting on an event, and making external remote procedure calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f1fc-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f1fc-147">Requirements</span></span>



| <span data-ttu-id="4f1fc-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f1fc-148">Requirement</span></span> | <span data-ttu-id="4f1fc-149">Value</span><span class="sxs-lookup"><span data-stu-id="4f1fc-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f1fc-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f1fc-150">Minimum supported client</span></span><br/> | <span data-ttu-id="4f1fc-151">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f1fc-151">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4f1fc-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f1fc-152">Minimum supported server</span></span><br/> | <span data-ttu-id="4f1fc-153">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f1fc-153">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4f1fc-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f1fc-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f1fc-155"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f1fc-155"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f1fc-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f1fc-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f1fc-157"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f1fc-157"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f1fc-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f1fc-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f1fc-159">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="4f1fc-159">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="4f1fc-160">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="4f1fc-160">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="4f1fc-161">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="4f1fc-161">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="4f1fc-162">**UnsubscribeServiceChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="4f1fc-162">**UnsubscribeServiceChangeNotifications**</span></span>](unsubscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="4f1fc-163">**QueryServiceDynamicInformation**</span><span class="sxs-lookup"><span data-stu-id="4f1fc-163">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

