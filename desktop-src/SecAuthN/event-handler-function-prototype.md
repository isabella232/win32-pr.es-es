---
description: Las funciones de prototipo de controlador de eventos se utilizan para todas las funciones que controlan eventos de notificación de Winlogon.
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: Función de controlador de eventos función de devolución de llamada prototipo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event_Handler_Function_Name
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 935ddac5660c814b898be17218d879678f2135ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652990"
---
# <a name="event-handler-function-prototype-callback-function"></a><span data-ttu-id="fa7a3-103">Función de controlador de eventos función de devolución de llamada prototipo</span><span class="sxs-lookup"><span data-stu-id="fa7a3-103">Event Handler Function Prototype callback function</span></span>

<span data-ttu-id="fa7a3-104">\[Las funciones de prototipo de controlador de eventos ya no están disponibles para su uso en Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fa7a3-104">\[Event Handler Prototype functions are no longer available for use as of Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="fa7a3-105">\]</span><span class="sxs-lookup"><span data-stu-id="fa7a3-105">\]</span></span>

<span data-ttu-id="fa7a3-106">Las funciones de prototipo de controlador de eventos se utilizan para todas las funciones que controlan eventos de notificación de [*Winlogon*](/windows/desktop/SecGloss/w-gly) .</span><span class="sxs-lookup"><span data-stu-id="fa7a3-106">Event Handler Prototype functions are used for all functions that handle [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification events.</span></span> <span data-ttu-id="fa7a3-107">El nombre de la función, que se representa a continuación por *el \_ \_ \_ nombre* de la función de controlador de eventos de marcador de posición, normalmente refleja el nombre del evento que controla la función.</span><span class="sxs-lookup"><span data-stu-id="fa7a3-107">The name of the function, represented below by the place holder *Event\_Handler\_Function\_Name*, typically reflects the name of the event that the function handles.</span></span> <span data-ttu-id="fa7a3-108">Por ejemplo, la función que controla los eventos de inicio de sesión podría tener el nombre: **WLEventLogon**.</span><span class="sxs-lookup"><span data-stu-id="fa7a3-108">For example, the function that handles logon events might be named: **WLEventLogon**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa7a3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa7a3-109">Syntax</span></span>


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="fa7a3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa7a3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa7a3-111">*Pinfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fa7a3-111">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa7a3-112">Puntero a una estructura [**de \_ \_ información de notificación WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) que contiene los detalles del evento.</span><span class="sxs-lookup"><span data-stu-id="fa7a3-112">A pointer to a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains the details of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa7a3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa7a3-113">Return value</span></span>

<span data-ttu-id="fa7a3-114">Esta función de devolución de llamada no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="fa7a3-114">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa7a3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa7a3-115">Remarks</span></span>

<span data-ttu-id="fa7a3-116">Si el controlador de eventos necesita crear procesos secundarios, debe llamar a la función [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="fa7a3-116">If your event handler needs to create child processes, it should call the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="fa7a3-117">De lo contrario, el nuevo proceso se creará en el escritorio de Winlogon, no en el escritorio del usuario.</span><span class="sxs-lookup"><span data-stu-id="fa7a3-117">Otherwise, the new process will be created on the Winlogon desktop, not the user's desktop.</span></span>

## <a name="examples"></a><span data-ttu-id="fa7a3-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fa7a3-118">Examples</span></span>

<span data-ttu-id="fa7a3-119">En el ejemplo siguiente se muestra cómo implementar controladores de eventos para eventos de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="fa7a3-119">The following sample shows how to implement event handlers for Winlogon events.</span></span> <span data-ttu-id="fa7a3-120">Para simplificar, solo se muestran las implementaciones de los controladores de eventos Logon y Logoff.</span><span class="sxs-lookup"><span data-stu-id="fa7a3-120">For simplicity, only the implementations of the Logon and Logoff event handlers are shown.</span></span> <span data-ttu-id="fa7a3-121">Puede implementar Controladores para el resto de los eventos exactamente de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="fa7a3-121">You can implement handlers for the rest of the events in exactly the same manner.</span></span>


```C++
// Copyright (C) Microsoft. All rights reserved. 
#include <windows.h>

// Here is the entrance function for the DLL.
BOOL WINAPI LibMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    switch (dwReason)
    {
        case DLL_PROCESS_ATTACH:
            {

             // Disable DLL_THREAD_ATTACH & DLL_THREAD_DETACH
             // notification calls. This is a performance optimization
             // for multithreaded applications that do not need 
             // thread-level notifications of attachment or
             // detachment.

            DisableThreadLibraryCalls (hInstance);
            }
            break;
    }

    return TRUE;
}

// Here is the event handler for the Winlogon Logon event.
void WLEventLogon (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogon.\r\n"));
}

// Here is the event handler for the Winlogon Logoff event.
void WLEventLogoff (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogff.\r\n"));
}
```



## <a name="requirements"></a><span data-ttu-id="fa7a3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa7a3-122">Requirements</span></span>



| <span data-ttu-id="fa7a3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa7a3-123">Requirement</span></span> | <span data-ttu-id="fa7a3-124">Value</span><span class="sxs-lookup"><span data-stu-id="fa7a3-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fa7a3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa7a3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fa7a3-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fa7a3-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fa7a3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa7a3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fa7a3-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa7a3-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fa7a3-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fa7a3-129">End of client support</span></span><br/>    | <span data-ttu-id="fa7a3-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fa7a3-130">Windows XP</span></span><br/>                                |
| <span data-ttu-id="fa7a3-131">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="fa7a3-131">End of server support</span></span><br/>    | <span data-ttu-id="fa7a3-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fa7a3-132">Windows Server 2003</span></span><br/>                       |



 

