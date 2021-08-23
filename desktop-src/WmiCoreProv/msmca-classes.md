---
description: Conjunto de clases WMI que exponen la arquitectura de comprobación de máquina (MCA). La capa de abstracción del sistema (SAL) proporciona todos los eventos notificados en la clase MSMCA. Intel Corporation desarrolla y posee el MCA.
ms.assetid: 4e35f871-5bce-49ed-a3e8-d2d967e6e2dc
title: Clases MSMCA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0f70bead9acbbb23fe0e2115ac12f967c7908f1f0eefa16d65cd1a57947e76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641085"
---
# <a name="msmca-classes"></a>Clases MSMCA

Las clases de Microsoft Machine Check Architecture (MSMCA) son un conjunto de clases WMI que exponen la arquitectura machine check (MCA). La capa de abstracción del sistema (SAL) proporciona todos los eventos notificados en la clase MSMCA. Intel Corporation desarrolla y posee el MCA.



| Clase                                                                               | Descripción                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**MSMCAEvent \_ CPUError**](msmcaevent-cpuerror.md)                                 | Representa un evento de error de CPU.                                                                          |
| [**Encabezado MSMCAEvent \_**](msmcaevent-header.md)                                     | Representa el encabezado común que usan todas las clases MSMCAEvent.                                          |
| [**InvalidError de MSMCAEvent \_**](msmcaevent-invaliderror.md)                         | Representa un error no válido de arquitectura de comprobación de memoria (MCA).                                            |
| [**MSMCAEvent \_ MemoryError**](msmcaevent-memoryerror.md)                           | Representa un evento de error de memoria MCA.                                                                  |
| [**MemoryPageRemoved de MSMCAEvent \_**](msmcaevent-memorypageremoved.md)               | Indica que el sistema operativo quitó una página física de memoria.                                 |
| [**MSMCAEvent \_ PCIBusError**](msmcaevent-pcibuserror.md)                           | Representa un error de bus PCI de MCA.                                                                       |
| [**MSMCAEvent \_ PCIComponentError**](msmcaevent-pcicomponenterror.md)               | Representa un error del componente PCI de MCA.                                                                 |
| [**MSMCAEvent \_ PlatformSpecificError**](msmcaevent-platformspecificerror.md)       | Representa un error específico de la plataforma MCA.                                                             |
| [**MSMCAEvent \_ SMBIOSError**](msmcaevent-smbioserror.md)                           | Representa un error de bios del sistema MCA.                                                                   |
| [**MSMCAEvent \_ SwitchToCMCPolling**](msmcaevent-switchtocmcpolling.md)             | Indica que el control de comprobación de la máquina corregido se cambia al sondeo.                            |
| [**SystemEventError de MSMCAEvent \_**](msmcaevent-systemeventerror.md)                 | Representa un error de evento del sistema MCA.                                                                  |
| [**MSMCAInfo**](msmcainfo.md)                                                      | Clase base abstracta de la que se derivan todas las clases de datos del proveedor machine check Architecture (MCA). |
| [**Entrada MSMCAInfo \_**](msmcainfo-entry.md)                                         | Representa una entrada de información MCA, Corrección de comprobación de máquina (CMC) o Error de plataforma corregido (CPE). |
| [**MSMCAInfo \_ RawCMCEvent**](msmcainfo-rawcmcevent.md)                             | Contiene un evento de CMC.                                                                                  |
| [**MSMCAInfo \_ RawCorrectedPlatformEvent**](msmcainfo-rawcorrectedplatformevent.md) | Contiene un evento de plataforma corregido.                                                                   |
| [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md)                               | Especifica los registros de MCA sin procesar.                                                                            |
| [**MSMCAInfo \_ RawMCAEvent**](msmcainfo-rawmcaevent.md)                             | Contiene un evento MCA.                                                                                  |
| [**WmiEvent**](wmievent.md)                                                        | Clase base abstracta de la que se derivan todas las clases de eventos del proveedor de MCA.                             |



 

 

 



