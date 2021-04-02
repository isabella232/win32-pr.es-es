---
description: El proceso de registro de eventos tiene lugar cuando un flujo selecciona el terminal.
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: Registrando eventos de terminal conectables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42bf75cfd0d7e6bd4d8a2520335c374cce28c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913814"
---
# <a name="registering-for-pluggable-terminal-events"></a><span data-ttu-id="f7ad1-103">Registrando eventos de terminal conectables</span><span class="sxs-lookup"><span data-stu-id="f7ad1-103">Registering for Pluggable Terminal Events</span></span>

<span data-ttu-id="f7ad1-104">El proceso de registro de eventos tiene lugar cuando un flujo selecciona el terminal.</span><span class="sxs-lookup"><span data-stu-id="f7ad1-104">The event registration process take place when the terminal is selected by a stream.</span></span> <span data-ttu-id="f7ad1-105">En la implementación de la aplicación terminal del método [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) , podemos usar la interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) del terminal que estaba conectada a la secuencia y llamar a **QueryInterface** para encontrar [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).</span><span class="sxs-lookup"><span data-stu-id="f7ad1-105">In the terminal application's implementation of the [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) method, we can use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of the terminal that was attached to the stream, and call **QueryInterface** to find [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).</span></span>

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

<span data-ttu-id="f7ad1-106">Si la llamada **QueryInterface** se realiza correctamente, podemos llamar al método [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) .</span><span class="sxs-lookup"><span data-stu-id="f7ad1-106">If the **QueryInterface** call succeeds, we can call the [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) method.</span></span> <span data-ttu-id="f7ad1-107">Para este propósito, debemos crear un objeto que implemente la interfaz [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) .</span><span class="sxs-lookup"><span data-stu-id="f7ad1-107">For this purpose, we should create an object that implements the [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) interface.</span></span> <span data-ttu-id="f7ad1-108">Pasamos esta interfaz como un parámetro del método **RegisterSink** .</span><span class="sxs-lookup"><span data-stu-id="f7ad1-108">We pass this interface as a parameter of the **RegisterSink** method.</span></span>

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

<span data-ttu-id="f7ad1-109">El terminal que implementa la llamada [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) almacenará la interfaz.</span><span class="sxs-lookup"><span data-stu-id="f7ad1-109">The terminal that implements the [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) call will store the interface.</span></span> <span data-ttu-id="f7ad1-110">El puntero se usará cuando el terminal desencadene un evento.</span><span class="sxs-lookup"><span data-stu-id="f7ad1-110">The pointer will be used when the terminal will fire an event.</span></span>

<span data-ttu-id="f7ad1-111">Se puede anular el registro del receptor de eventos mediante [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).</span><span class="sxs-lookup"><span data-stu-id="f7ad1-111">The event sink can be unregistered using [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).</span></span>

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
