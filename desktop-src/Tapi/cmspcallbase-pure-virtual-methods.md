---
description: Estos métodos deben reemplazarse por clases derivadas.
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Métodos virtuales puros de CMSPCallBase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d8dea4c1a240e362a4dc3a19b3c09a37a318947
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103909997"
---
# <a name="cmspcallbase-pure-virtual-methods"></a>Métodos virtuales puros de CMSPCallBase

Estos métodos deben reemplazarse por clases derivadas.



| Métodos virtuales puros de CMSPCallBase                                 | Descripción                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPCallAddRef**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | Método AddRef privado para el objeto de llamada.                                                                                              |
| [**MSPCallRelease**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | Método de liberación privado para el objeto de llamada.                                                                                             |
| [**Smss**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | Lo llama el objeto de dirección MSP (en el método [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) para inicializar el objeto de llamada MSP. |
| [**Apagado**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | Lo llama el objeto de dirección MSP para cerrar la llamada.                                                                                |
| [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | Llamado por [**CreateStream (**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) para crear un objeto de flujo.                                               |
| [**CreateStreamObject**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | Llamado por [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) para crear un objeto de flujo.                                  |
| [**RemoveStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | La aplicación llama a este método para quitar un flujo de la llamada.                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
