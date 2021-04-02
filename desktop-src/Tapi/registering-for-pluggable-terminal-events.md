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
# <a name="registering-for-pluggable-terminal-events"></a>Registrando eventos de terminal conectables

El proceso de registro de eventos tiene lugar cuando un flujo selecciona el terminal. En la implementación de la aplicación terminal del método [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) , podemos usar la interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) del terminal que estaba conectada a la secuencia y llamar a **QueryInterface** para encontrar [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

Si la llamada **QueryInterface** se realiza correctamente, podemos llamar al método [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) . Para este propósito, debemos crear un objeto que implemente la interfaz [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) . Pasamos esta interfaz como un parámetro del método **RegisterSink** .

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

El terminal que implementa la llamada [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) almacenará la interfaz. El puntero se usará cuando el terminal desencadene un evento.

Se puede anular el registro del receptor de eventos mediante [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
