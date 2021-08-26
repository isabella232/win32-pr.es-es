---
description: En el ejemplo de código siguiente se muestra una transferencia de llamadas.
ms.assetid: 05862605-2600-4cdf-8390-e24e4e8586f3
title: Transferir una llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71d6e6fd9dc275a6d4c00e84806132cabf756effcb41e7a704b20929bc46d1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072835"
---
# <a name="transfer-a-call"></a>Transferir una llamada

En el ejemplo de código siguiente se muestra una transferencia de llamadas.

Antes de usar este ejemplo de código, una llamada debe estar en curso y debe realizar las operaciones en [Realizar](make-a-call.md) una llamada [o Recibir una llamada .](receive-a-call.md)

> [!Note]  
> Este ejemplo no tiene la comprobación de errores y las versiones adecuadas para el código de producción.

 

``` syntax
// From elsewhere in your code, you have obtained pAddress and pBasicCall, 
// which are pointers to the ITAddress and ITBasicCallControl interfaces
// of the call in progress that will be transferred.

// Create the call object for transfer. bstrAddressToCall and dwAddressType
// have been retrieved from a UI.
ITBasicCallControl * pConsultCall
HRESULT hr = pAddress->CreateCall(
        bstrAddressToCall,
        dwAddressType,
        &pConsultCall
        );
// If ( hr != S_OK ) process the error here. 

// Start the transfer.
hr = pBasicCall->Transfer(
        pConsultCall,
        VARIANT_TRUE
        );
// If ( hr != S_OK ) process the error here. 

// Depending on the service provider, additional operations may be available
// or required.

// Finish the transfer.
hr = pConsultCall->Finish(FM_ASTRANSFER);
// If ( hr != S_OK ) process the error here. 

// The consultation call transitions to CS_DISCONNECTED.
// The objects associated with pConsultCall and pBasicCall can be released immediately or
// used for information purposes and released later.
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)
</dt> </dl>

 

 



