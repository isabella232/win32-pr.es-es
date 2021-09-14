---
description: En el ejemplo de código siguiente se muestra la creación de una llamada de conferencia simple. Para obtener información sobre las videoconferencias multimedia de multidifusión IP, consulte About Rendezvous IP Telephony Conferencing (Acerca de la conferencia de telefonía IP de Encuentro).
ms.assetid: fb55853d-b882-41c8-99e6-bfa897b2dabf
title: Creación de una conferencia simple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa0bfd8fede9fa61aedb6b630a2451803e2257d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073506"
---
# <a name="create-a-simple-conference"></a>Creación de una conferencia simple

En el ejemplo de código siguiente se muestra la creación de una llamada de conferencia simple. Para obtener información sobre las videoconferencias multimedia de multidifusión IP, vea [About Rendezvous IP Telephony Conferencing](about-rendezvous-ip-telephony-conferencing.md).

Antes de usar este ejemplo de código, debe haber una [](make-a-call.md) llamada [en](receive-a-call.md) curso y debe realizar las operaciones realizadas en Realizar una llamada o Recibir una llamada.

> [!Note]  
> Este ejemplo no tiene la comprobación de errores y las versiones adecuadas para el código de producción.

 

``` syntax
// From elsewhere in your code, you have obtained pBasicCall and pCallInfo, 
// which are pointers to the ITBasicCallControl and ITCallInfo interfaces
// of a call currently in progress. pAddress is an ITAddress pointer.

// Create a consultation call for the conference.
ITBasicCallControl *pConsultCall;
HRESULT hr = pAddress->CreateCall(
        bstrAddressToCall,
        dwAddressType,
        &pConsultCall
        );
// If ( hr != S_OK ) process the error here. 

// Move the consultation call into your conference.
// Note: If a CallHub object does not already exist, TAPI will create it.
hr = pBasicCall->Conference(
               pConsultCall,
               VARIANT_TRUE
               );
// If ( hr != S_OK ) process the error here. 

// Finish the creation of the conference.
hr = pConsultCall->Finish(FM_ASCONFERENCE);
// If ( hr != S_OK ) process the error here. 

// Assuming the Finish method succeeds, the consultation call (pConsultCall)
// may transition to the CS_DISCONNECTED state or may remain connected, 
// depending on the service provider.
//
// Get the ITCallHub interface pointer.
ITCallHub *pCallHub;
hr = pCallInfo->get_CallHub( pCallHub );
// If ( hr != S_OK ) process the error here. 

// You can use the ITCallHub interface to obtain additional information on
// the conference. Specific capabilities depend on the TSP/MSP being used.
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)
</dt> </dl>

 

 



