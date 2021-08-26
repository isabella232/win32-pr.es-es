---
description: El siguiente material proporciona detalles sobre las clases base del proveedor de Media Service.
ms.assetid: ef845c44-1ff5-42a1-8e91-38d66e6fe363
title: Referencia de clases base de MSP de TAPI 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1c0b2f19f372e60972c66d965f689ec79f930f343080be21471fbc4ba59f67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905745"
---
# <a name="tapi-3-msp-base-classes-reference"></a>Referencia de clases base de MSP de TAPI 3

El siguiente material proporciona detalles sobre las clases base del proveedor de Media Service.



| Clases base del proveedor de servicios multimedia (orden alfabético) | Descripción                                                                                                                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CAudioCaptureTerminal](caudiocaptureterminal.md)       | Se deriva de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminal de captura de audio estático para dispositivos de onda mediante el DirectShow wavein. Se define en MSPtmac.h.               |
| [CAudioRenderTerminal](caudiorenderterminal.md)         | Se deriva de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminal de representación de audio estático para dispositivos de onda mediante el DirectShow de onda. Se define en MSPtrmar.h.              |
| [CBaseTerminal](cbaseterminal.md)                       | Una clase base de terminal aplicable a los terminales estáticos y dinámicos. Es completamente genérico, por lo que cualquier implementación terminal puede derivar de esta clase directa o indirectamente. Definido en MSPterm.h |
| [**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)                       | Implementa el objeto de dirección MSP y admite la [**interfaz ITMSPAddress.**](/windows/desktop/api/msp/nn-msp-itmspaddress) Se define en MSPaddr.h.                                                                                |
| [CMSPArray](cmsparray.md)                               | Plantilla que implementa una matriz inteligente que crecerá a petición. Se define en MSPutils.h.                                                                                                               |
| [**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)                     | Proporciona una implementación genérica del objeto de llamada y admite la [**interfaz ITStreamControl.**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) Se define en MSPcall.h.                                                       |
| [**CMSPCallMultiGraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)         | Define una llamada que usa un gráfico de filtro para cada secuencia. Se define en MSPcall.h.                                                                                                                          |
| [**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)                         | Expone métodos que permiten a una aplicación iniciar, pausar o detener una subtransmisión y seleccionar o anular la selección de terminales. Se define en MSPstrm.h.                                                              |
| [CMSPThread](cmspthread.md)                             | Implementa el subproceso de trabajo del MSP. Se define en MSPthrd.h.                                                                                                                                               |
| [CSingleFilterTerminal](csinglefilterterminal.md)       | Una clase base de terminal adicional aplicable a los terminales estáticos y dinámicos. Hace que la implementación sea más específica suponiendo que el terminal tiene un único DirectShow filtro. Se define en MSPterm.h.    |
| [CVideoCaptureTerminal](cvideocaptureterminal.md)       | Se deriva de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminal de captura de vídeo estático mediante un único DirectShow filtro. Se define en MSPtmvc.h.                                  |



 

 

 
