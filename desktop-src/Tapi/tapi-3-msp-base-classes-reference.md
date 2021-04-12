---
description: En el material siguiente se proporcionan detalles sobre las clases base del proveedor de servicios multimedia.
ms.assetid: ef845c44-1ff5-42a1-8e91-38d66e6fe363
title: Referencia de las clases base de TAPI 3 MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4cca24b69a645b18cc0950288e0de983b54355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276793"
---
# <a name="tapi-3-msp-base-classes-reference"></a>Referencia de las clases base de TAPI 3 MSP

En el material siguiente se proporcionan detalles sobre las clases base del proveedor de servicios multimedia.



| Clases base de proveedores de servicios multimedia (orden alfabético) | Descripción                                                                                                                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CAudioCaptureTerminal](caudiocaptureterminal.md)       | Se deriva de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminal de captura de audio estático para dispositivos de onda mediante el filtro de onda de DirectShow. Definido en MSPtmac. h.               |
| [CAudioRenderTerminal](caudiorenderterminal.md)         | Se deriva de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminal de representación de audio estático para dispositivos de onda mediante el filtro WaveOut de DirectShow. Definido en MSPtrmar. h.              |
| [CBaseTerminal](cbaseterminal.md)                       | Una clase base de terminal aplicable a los terminales estáticos y dinámicos. Es completamente genérico, por lo que cualquier implementación de terminal puede derivar de esta clase directa o indirectamente. Definido en MSPterm. h |
| [**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)                       | Implementa el objeto de dirección MSP y admite la interfaz [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) . Definido en MSPaddr. h.                                                                                |
| [CMSPArray](cmsparray.md)                               | Plantilla que implementa una matriz inteligente que crecerá a petición. Definido en MSPutils. h.                                                                                                               |
| [**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)                     | Proporciona una implementación genérica del objeto Call y admite la interfaz [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) . Definido en MSPcall. h.                                                       |
| [**CMSPCallMultiGraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)         | Define una llamada que usa un gráfico de filtro para cada flujo. Definido en MSPcall. h.                                                                                                                          |
| [**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)                         | Expone métodos que permiten a una aplicación iniciar, pausar o detener una subsecuencia, y seleccionar o anular la selección de terminales. Definido en MSPstrm. h.                                                              |
| [CMSPThread](cmspthread.md)                             | Implementa el subproceso de trabajo de MSP. Definido en MSPthrd. h.                                                                                                                                               |
| [CSingleFilterTerminal](csinglefilterterminal.md)       | Clase base de terminal adicional aplicable a los terminales estáticos y dinámicos. Hace que la implementación sea más específica suponiendo que el terminal tiene un solo filtro DirectShow. Definido en MSPterm. h.    |
| [CVideoCaptureTerminal](cvideocaptureterminal.md)       | Se deriva de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminal de captura de vídeo estático con un solo filtro DirectShow. Definido en MSPtmvc. h.                                  |



 

 

 
