---
description: En el ejemplo de código siguiente se muestra el uso del objeto TAPI para examinar los recursos de telefonía disponibles para una dirección que pueda controlar un conjunto especificado de requisitos de tipo multimedia. En este ejemplo, el audio y el vídeo son los medios necesarios.
ms.assetid: 8be40a87-931d-4cda-9ef7-f9c0489e0b7b
title: Selección de una dirección
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 1da79ffa0f2bd3264bb97e0c78eebe7b06045c63ec927d709fffef2786e2870c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072845"
---
# <a name="select-an-address"></a>Selección de una dirección

En el ejemplo de código siguiente se muestra el uso del objeto TAPI para examinar los recursos de telefonía disponibles para una dirección que pueda controlar un conjunto especificado de requisitos de tipo multimedia. En este ejemplo, el audio y el vídeo son los medios necesarios.

Antes de usar este ejemplo de código, debe realizar las operaciones en [Inicializar TAPI](initialize-tapi.md).

> [!NOTE]  
> Este ejemplo no tiene la comprobación de errores y las versiones adecuadas para el código de producción.

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

## <a name="related-topics"></a>Temas relacionados

[ITTAPI::EnumerateAddresses](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)

[ITMediaSupport](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)

[Constantes TAPIMEDIATYPE \_](tapimediatype--constants.md)
