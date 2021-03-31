---
description: Un conjunto de clases WMI que exponen la arquitectura de comprobación automática (MCA). La capa de abstracción del sistema (SAL) proporciona todos los eventos que se indican en la clase MSMCA. Intel Corporation desarrolla y posee la MCA.
ms.assetid: 4e35f871-5bce-49ed-a3e8-d2d967e6e2dc
title: Clases MSMCA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461d4c5c50ae5316c96c3dffc18af7b729cfa6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361010"
---
# <a name="msmca-classes"></a>Clases MSMCA

Las clases de arquitectura de Microsoft Machine check (MSMCA) son un conjunto de clases WMI que exponen la arquitectura de comprobación de la máquina (MCA). La capa de abstracción del sistema (SAL) proporciona todos los eventos que se indican en la clase MSMCA. Intel Corporation desarrolla y posee la MCA.



| Clase                                                                               | Descripción                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**MSMCAEvent \_ CPUError**](msmcaevent-cpuerror.md)                                 | Representa un evento de error de CPU.                                                                          |
| [**\_Encabezado MSMCAEvent**](msmcaevent-header.md)                                     | Representa el encabezado común que usan todas las clases MSMCAEvent.                                          |
| [**MSMCAEvent \_ InvalidError**](msmcaevent-invaliderror.md)                         | Representa un error no válido de arquitectura de comprobación de memoria (MCA).                                            |
| [**MSMCAEvent \_ MemoryError**](msmcaevent-memoryerror.md)                           | Representa un evento de error de memoria MCA.                                                                  |
| [**MSMCAEvent \_ MemoryPageRemoved**](msmcaevent-memorypageremoved.md)               | Indica que el sistema operativo ha quitado una página física de memoria.                                 |
| [**MSMCAEvent \_ PCIBusError**](msmcaevent-pcibuserror.md)                           | Representa un error de bus PCI de MCA.                                                                       |
| [**MSMCAEvent \_ PCIComponentError**](msmcaevent-pcicomponenterror.md)               | Representa un error de componente PCI MCA.                                                                 |
| [**MSMCAEvent \_ PlatformSpecificError**](msmcaevent-platformspecificerror.md)       | Representa un error específico de la plataforma MCA.                                                             |
| [**MSMCAEvent \_ SMBIOSError**](msmcaevent-smbioserror.md)                           | Representa un error del BIOS del sistema MCA.                                                                   |
| [**MSMCAEvent \_ SwitchToCMCPolling**](msmcaevent-switchtocmcpolling.md)             | Indica que el control de comprobación de máquina corregido se ha cambiado a sondeo.                            |
| [**MSMCAEvent \_ SystemEventError**](msmcaevent-systemeventerror.md)                 | Representa un error de evento del sistema MCA.                                                                  |
| [**MSMCAInfo**](msmcainfo.md)                                                      | Clase base abstracta de la que se derivan todas las clases de datos del proveedor de la arquitectura de comprobación de equipo (MCA). |
| [**\_Entrada MSMCAInfo**](msmcainfo-entry.md)                                         | Representa una entrada de información de MCA, corrección de máquina corregida (CMC) o error de plataforma corregida (CPE). |
| [**MSMCAInfo \_ RawCMCEvent**](msmcainfo-rawcmcevent.md)                             | Contiene un evento CMC.                                                                                  |
| [**MSMCAInfo \_ RawCorrectedPlatformEvent**](msmcainfo-rawcorrectedplatformevent.md) | Contiene un evento de plataforma corregido.                                                                   |
| [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md)                               | Especifica los registros de MCA sin formato.                                                                            |
| [**MSMCAInfo \_ RawMCAEvent**](msmcainfo-rawmcaevent.md)                             | Contiene un evento de MCA.                                                                                  |
| [**WmiEvent**](wmievent.md)                                                        | Clase base abstracta de la que se derivan todas las clases de eventos de proveedor MCA.                             |



 

 

 



