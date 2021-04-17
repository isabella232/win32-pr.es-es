---
description: En el ejemplo de código siguiente se muestra el uso del objeto TAPI para examinar los recursos de telefonía disponibles para una dirección que puede controlar un conjunto especificado de requisitos de tipos de medios. En este ejemplo, audio y vídeo son los medios necesarios.
ms.assetid: 8be40a87-931d-4cda-9ef7-f9c0489e0b7b
title: Seleccionar una dirección
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: da41059c38328ff00271e4fa561561eecf83e1cb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105689902"
---
# <a name="select-an-address"></a><span data-ttu-id="0c273-104">Seleccionar una dirección</span><span class="sxs-lookup"><span data-stu-id="0c273-104">Select an Address</span></span>

<span data-ttu-id="0c273-105">En el ejemplo de código siguiente se muestra el uso del objeto TAPI para examinar los recursos de telefonía disponibles para una dirección que puede controlar un conjunto especificado de requisitos de tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="0c273-105">The following code example demonstrates use of the TAPI object to examine available telephony resources for an address that can handle a specified set of media type requirements.</span></span> <span data-ttu-id="0c273-106">En este ejemplo, audio y vídeo son los medios necesarios.</span><span class="sxs-lookup"><span data-stu-id="0c273-106">In this example, audio and video are the required media.</span></span>

<span data-ttu-id="0c273-107">Antes de usar este ejemplo de código, debe realizar las operaciones en [Initialize TAPI](initialize-tapi.md).</span><span class="sxs-lookup"><span data-stu-id="0c273-107">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="0c273-108">Este ejemplo no tiene la comprobación de errores y las versiones adecuadas para el código de producción.</span><span class="sxs-lookup"><span data-stu-id="0c273-108">This example doesn't have the error checking and releases appropriate for production code.</span></span>

```cpp
// Declare the interfaces used to select an address.
IEnumAddress * pIEnumAddress;
ITAddress * pAddress;
ITMediaSupport * pMediaSupport;

// Use the TAPI object to enumerate available addresses.
hr = gpTapi->EnumerateAddresses( &pIEnumAddress );
// If (hr != S_OK) process the error here. 

// Locate an address that can support the media type the application needs.
while ( S_OK == pIEnumAddress->Next(1, &pAddress, NULL) )
{
    // Determine the media support.
    hr = pAddress->QueryInterface(
         IID_ITMediaSupport,
         (void **)&pMediaSupport
         );
    // If (hr != S_OK) process the error here. 

    // In this example, the required media type is already known.
    // The application can also use the address object to
    // enumerate the media supported, then choose from there.
    hr = pMediaSupport->QueryMediaType(
         TAPIMEDIATYPE_AUDIO|TAPIMEDIATYPE_VIDEO,
         &bSupport
         );
    // If (hr != S_OK) process the error here. 

    if (bSupport)
    {
        break;
    }
}
// pAddress is now a usable address.
```

## <a name="related-topics"></a><span data-ttu-id="0c273-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0c273-109">Related topics</span></span>

[<span data-ttu-id="0c273-110">ITTAPI::EnumerateAddresses</span><span class="sxs-lookup"><span data-stu-id="0c273-110">ITTAPI::EnumerateAddresses</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)

[<span data-ttu-id="0c273-111">ITMediaSupport</span><span class="sxs-lookup"><span data-stu-id="0c273-111">ITMediaSupport</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)

[<span data-ttu-id="0c273-112">Constantes de TAPIMEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="0c273-112">TAPIMEDIATYPE\_ Constants</span></span>](tapimediatype--constants.md)
