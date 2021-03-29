---
title: Supervisión de conexiones y desconexiones de sesión
description: Para registrar una aplicación con Servicios de Escritorio remoto, almacene el nombre de la aplicación de servidor de canal virtual en el registro mediante la adición de una subclave.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e819b13594ecec14a2b425560152cadedd4e9122
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077856"
---
# <a name="monitoring-session-connections-and-disconnections"></a><span data-ttu-id="3851d-103">Supervisión de conexiones y desconexiones de sesión</span><span class="sxs-lookup"><span data-stu-id="3851d-103">Monitoring session connections and disconnections</span></span>

<span data-ttu-id="3851d-104">Para una aplicación de servicio, como una aplicación de servidor de canal virtual, para supervisar las conexiones y desconexiones de la sesión, debe registrarla con Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="3851d-104">For a service application, such as a virtual channel server application, to monitor session connections and disconnections, you must register it with Remote Desktop Services.</span></span> <span data-ttu-id="3851d-105">Para registrar la aplicación con Servicios de Escritorio remoto, almacene el nombre de la aplicación de servidor de canal virtual en el registro agregando una subclave en la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="3851d-105">To register the application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="3851d-106">**HKEY \_ \_Equipo local** \\ **System** \\ **CurrentControlSet** \\ **control** \\ **TerminalServer** \\ **AddIns**</span><span class="sxs-lookup"><span data-stu-id="3851d-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**</span></span>

<span data-ttu-id="3851d-107">La subclave puede tener cualquier nombre.</span><span class="sxs-lookup"><span data-stu-id="3851d-107">The subkey can have any name.</span></span> <span data-ttu-id="3851d-108">Debe tener un valor **reg \_ SZ** , **Name**, que contiene el nombre simbólico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3851d-108">It must have a **REG\_SZ** value, **Name**, that contains the symbolic name of the application.</span></span>

``` syntax
Name = AddinName
```

<span data-ttu-id="3851d-109">La longitud máxima de la subclave y del valor de **Name** es de 99 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3851d-109">The maximum length of both the subkey and the value of **Name** is 99 characters.</span></span>

<span data-ttu-id="3851d-110">La subclave también debe tener un valor de **Registro \_ DWORD** que indique el tipo de aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="3851d-110">The subkey must also have a **REG\_DWORD** value that indicates the type of server application.</span></span>

``` syntax
Type = AddinType
```

<span data-ttu-id="3851d-111">*AddinType* debe ser el siguiente valor.</span><span class="sxs-lookup"><span data-stu-id="3851d-111">*AddinType* must be the following value.</span></span>



| <span data-ttu-id="3851d-112">Value</span><span class="sxs-lookup"><span data-stu-id="3851d-112">Value</span></span> | <span data-ttu-id="3851d-113">Significado</span><span class="sxs-lookup"><span data-stu-id="3851d-113">Meaning</span></span>                               |
|-------|---------------------------------------|
| <span data-ttu-id="3851d-114">3</span><span class="sxs-lookup"><span data-stu-id="3851d-114">3</span></span>     | <span data-ttu-id="3851d-115">Aplicación de modo de usuario, espacio de sesión.</span><span class="sxs-lookup"><span data-stu-id="3851d-115">User-mode application, session space.</span></span> |



 

<span data-ttu-id="3851d-116">El registro de la aplicación de servicio solo surte efecto en las sesiones creadas después de realizar el registro.</span><span class="sxs-lookup"><span data-stu-id="3851d-116">Registration of the service application takes effect only in sessions created after the registration was performed.</span></span>

<span data-ttu-id="3851d-117">Para cada aplicación de servicio registrada, Servicios de Escritorio remoto señalará un conjunto de objetos de eventos cuando un cliente se conecta o desconecta de la sesión.</span><span class="sxs-lookup"><span data-stu-id="3851d-117">For each registered service application, Remote Desktop Services will signal a set of event objects when a client connects or disconnects from the session.</span></span> <span data-ttu-id="3851d-118">Cada complemento de canal virtual debe registrarse y crear los eventos de notificación llamando a [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa).</span><span class="sxs-lookup"><span data-stu-id="3851d-118">Each virtual channel plug-in must register itself and create the notification events by calling [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa).</span></span> <span data-ttu-id="3851d-119">Los nombres de estos objetos de evento se ajustan al formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="3851d-119">The names of these event objects adhere to the following format.</span></span>

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

<span data-ttu-id="3851d-120">*AddinName* es la cadena especificada en el valor de **nombre** de la subclave del registro en la que se registra la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="3851d-120">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="3851d-121">Al crear estos eventos en una sesión, se crean en un directorio de eventos especial por sesión.</span><span class="sxs-lookup"><span data-stu-id="3851d-121">Creating these events under a session causes them to be created in a special per-session event directory.</span></span> <span data-ttu-id="3851d-122">El directorio de eventos proporciona seguridad adicional al impedir que las aplicaciones de otras sesiones modifiquen el estado de estos eventos.</span><span class="sxs-lookup"><span data-stu-id="3851d-122">The event directory provides added security by preventing applications in other sessions from modifying the state of these events.</span></span>

<span data-ttu-id="3851d-123">Para controlar si se reciben los eventos de reconexión y de desconexión en el servidor, puede colocar la marca **RemoteControlPersistent** en el registro con la siguiente clave:</span><span class="sxs-lookup"><span data-stu-id="3851d-123">To control whether RECONNECT and DISCONNECT events are received on the server, you can place the **RemoteControlPersistent** flag in the registry under the following key:</span></span>

<span data-ttu-id="3851d-124">**HKEY \_ \_Equipo local** \\ **System** \\ **CurrentControlSet** \\ **control** \\ **TerminalServer** \\ **AddIns** \\ *addinname*</span><span class="sxs-lookup"><span data-stu-id="3851d-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**\\*addinname*</span></span>

<span data-ttu-id="3851d-125">La marca habilita o deshabilita la señalización de los eventos de reconexión y desconexión cuando se inicia o se detiene una sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="3851d-125">The flag enables or disables RECONNECT and DISCONNECT events from being signaled when a client session starts or stops.</span></span> <span data-ttu-id="3851d-126">La sintaxis del valor de **reg \_ DWORD** es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="3851d-126">The syntax of the **REG\_DWORD** value is the following.</span></span>

``` syntax
RemoteControlPersistent = flag
```

<span data-ttu-id="3851d-127">El valor de *Flag* puede ser uno o cero.</span><span class="sxs-lookup"><span data-stu-id="3851d-127">The value of *flag* can be one or zero.</span></span> <span data-ttu-id="3851d-128">Cero es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3851d-128">Zero is the default value.</span></span> <span data-ttu-id="3851d-129">Si se establece en uno, no se notificará a la aplicación de servicio si la sesión del cliente se inicia o se detiene.</span><span class="sxs-lookup"><span data-stu-id="3851d-129">If set to one, the service application will not be notified if the client session is started or stopped.</span></span> <span data-ttu-id="3851d-130">Si se establece en cero, se señalará un evento de reconexión cuando se inicie la sesión del cliente y se señalará un evento de desconexión cuando se detenga la sesión del cliente.</span><span class="sxs-lookup"><span data-stu-id="3851d-130">If set to zero, a RECONNECT event is signaled when the client session starts, and a DISCONNECT event is signaled when the client session stops.</span></span>

<span data-ttu-id="3851d-131">Todavía se admite el formato de nombre de objeto de evento anterior en Windows Server 2008 para mantener la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3851d-131">The previous event-object name format is still supported in Windows Server 2008 for backward compatibility.</span></span> <span data-ttu-id="3851d-132">Se recomienda usar el formato más reciente de Windows Server 2008 porque es más seguro.</span><span class="sxs-lookup"><span data-stu-id="3851d-132">It is recommended that you use the newer Windows Server 2008 format because it is more secure.</span></span>

<span data-ttu-id="3851d-133">El formato de evento anterior es el siguiente.</span><span class="sxs-lookup"><span data-stu-id="3851d-133">The previous event format is as follows.</span></span>

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

<span data-ttu-id="3851d-134">*AddinName* es la cadena especificada en el valor de **nombre** de la subclave del registro en la que se registra la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="3851d-134">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="3851d-135">*SessionID* es el identificador de sesión de una sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="3851d-135">*SessionId* is the session identifier of a client session.</span></span>

 

 