---
description: 'Métodos virtuales puros de CMSPCallBase: estas clases derivadas deben invalidar estos métodos.'
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Métodos virtuales puros de CMSPCallBase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da8530ab3dae737bf1407f00d5d4a415a1437e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094463"
---
# <a name="cmspcallbase-pure-virtual-methods"></a>Métodos virtuales puros de CMSPCallBase

Estas clases derivadas deben invalidar estos métodos.



| Métodos virtuales puros de CMSPCallBase                                 | Descripción                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPCallAddRef**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | Método AddRef privado para el objeto de llamada.                                                                                              |
| [**MSPCallRelease**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | Método Private Release para el objeto de llamada.                                                                                             |
| [**Init**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | Llamado por el objeto de dirección MSP (en el [**método CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) para inicializar el objeto de llamada MSP. |
| [**Apagado**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | Llamado por el objeto de dirección MSP para apagar la llamada.                                                                                |
| [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | Lo llama [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) para crear un objeto de secuencia.                                               |
| [**CreateStreamObject**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | [**InternalCreateStream llama a para**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) crear un objeto de secuencia.                                  |
| [**RemoveStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | Llamado por la aplicación para quitar una secuencia de la llamada                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
