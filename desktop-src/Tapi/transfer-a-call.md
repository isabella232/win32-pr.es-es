---
description: En el ejemplo de código siguiente se muestra una transferencia de llamada.
ms.assetid: 05862605-2600-4cdf-8390-e24e4e8586f3
title: Transferir una llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1d537efd33ea2df4ddb9ad3e9b55b633cca18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678201"
---
# <a name="transfer-a-call"></a><span data-ttu-id="b2f93-103">Transferir una llamada</span><span class="sxs-lookup"><span data-stu-id="b2f93-103">Transfer a Call</span></span>

<span data-ttu-id="b2f93-104">En el ejemplo de código siguiente se muestra una transferencia de llamada.</span><span class="sxs-lookup"><span data-stu-id="b2f93-104">The following code example demonstrates a call transfer.</span></span>

<span data-ttu-id="b2f93-105">Antes de usar este ejemplo de código, una llamada debe estar en curso y debe realizar las operaciones en [realizar una llamada](make-a-call.md) o [recibir una llamada](receive-a-call.md).</span><span class="sxs-lookup"><span data-stu-id="b2f93-105">Before using this code example, a call must be in progress, and you must perform the operations in [Make a Call](make-a-call.md) or [Receive a Call](receive-a-call.md).</span></span>

> [!Note]  
> <span data-ttu-id="b2f93-106">Este ejemplo no tiene la comprobación de errores y las versiones adecuadas para el código de producción.</span><span class="sxs-lookup"><span data-stu-id="b2f93-106">This example does not have the error checking and releases appropriate for production code.</span></span>

 

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

## <a name="related-topics"></a><span data-ttu-id="b2f93-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2f93-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2f93-108">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="b2f93-108">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="b2f93-109">**ITBasicCallControl**</span><span class="sxs-lookup"><span data-stu-id="b2f93-109">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="b2f93-110">**ITCallHub**</span><span class="sxs-lookup"><span data-stu-id="b2f93-110">**ITCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)
</dt> </dl>

 

 



