---
description: 'CmSPAddress Pure Virtual Methods : estas clases derivadas deben reemplazar estos métodos.'
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: Métodos virtuales puros de CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d9b9494e4ee42972d97433927fd587034af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084213"
---
# <a name="cmspaddress-pure-virtual-methods"></a>Métodos virtuales puros de CMSPAddress

Estos métodos deben reemplazarse por clases derivadas.



| Métodos virtuales puros de CMSPAddress                           | Descripción                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | Método AddRef privado para la dirección.                                                                                                                                                 |
| [**MSPAddressRelease**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | Método Private Release para la dirección.                                                                                                                                                |
| [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | TapI llama a para crear un objeto de llamada. La implementación de la clase derivada simplemente debe llamar a la [**función CreateMSPCallHelper.**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper)        |
| [**ShutdownMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | Lo llama TAPI para apagar un objeto de llamada. La implementación de la clase derivada simplemente debe llamar a la [**función ShutdownMSPCallHelper.**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) |
| [**GetCallMediaTypes**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | Obtiene los tipos de medios admitidos por el MSP.                                                                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



