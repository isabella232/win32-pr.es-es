---
description: El proceso de registro de eventos tiene lugar cuando una secuencia selecciona el terminal.
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: Registro de eventos de terminal conectable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71993d597cbcba7c634068813eb14939539dc7e7d43cda0105e8cf9ee615a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060463"
---
# <a name="registering-for-pluggable-terminal-events"></a>Registro de eventos de terminal conectable

El proceso de registro de eventos tiene lugar cuando una secuencia selecciona el terminal. En la implementación de la aplicación terminal del método [**SelectTerminal,**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) podemos usar la interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) del terminal que se ha asociado a la secuencia y llamar a **QueryInterface** para buscar [**ITPluggableTerminalEventSinkRegistration.**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

Si la **llamada a QueryInterface** se realiza correctamente, podemos llamar al [**método RegisterSink.**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) Para ello, debemos crear un objeto que implemente la interfaz [**ITPluggableTerminalEventSink.**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) Se pasa esta interfaz como parámetro del **método RegisterSink.**

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

El terminal que implementa la llamada [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) almacenará la interfaz. El puntero se usará cuando el terminal desplace un evento.

El receptor de eventos se puede anular el registro [**mediante UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
