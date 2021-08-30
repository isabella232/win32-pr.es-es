---
description: En la tabla siguiente se enumeran los objetos COM y las interfaces asociadas a los controles de conferencia Rendezvous.
ms.assetid: d9634586-8315-46d3-9ffc-bfa9a4d7738e
title: Interfaces COM de Encuentro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05978b3536b2bb6d3cb384372c00f9052c2d602b51fb52e79f88d6f8eff2ca32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080485"
---
# <a name="rendezvous-com-interfaces"></a>Interfaces COM de Encuentro

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

En la tabla siguiente se enumeran los objetos COM y las interfaces asociadas a los controles de conferencia Rendezvous.

Para obtener información adicional sobre el modelo de objetos componentes (COM), consulte las secciones pertinentes del Kit de desarrollo de software de plataforma (SDK).



| Interfaces                                                         | Descripción                                                                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**IEnumDialableAddrs**](/windows/desktop/api/Rend/nn-rend-ienumdialableaddrs)                   | Enumera las direcciones que se pueden marcar disponibles en el directorio actual.                                                     |
| [**IEnumDirectory**](/windows/desktop/api/Rend/nn-rend-ienumdirectory)                           | Enumera los objetos [**ITDirectory.**](/windows/desktop/api/Rend/nn-rend-itdirectory)                                                                    |
| [**IEnumDirectoryObject**](/windows/desktop/api/Rend/nn-rend-ienumdirectoryobject)               | Enumera los objetos [**ITDirectoryObject.**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)                                                        |
| [**IEnumMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)                         | Enumera los [**objetos IMcastScope.**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)                                                                    |
| [**IEnumMedia**](ienummedia.md)                                   | Enumera los [**objetos ITMedia.**](itmedia.md)                                                                            |
| [**IEnumTime**](ienumtime.md)                                     | Enumera los objetos [**ITTime.**](ittime.md)                                                                              |
| [**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)         | Interfaz principal para el contenedor COM de asignación de direcciones de multidifusión.                                                           |
| [**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)                         | Proporciona métodos para recuperar y establecer la información de concesión de direcciones.                                                           |
| [**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)                                 | Encapsula todas las propiedades de un ámbito de multidifusión y proporciona métodos para obtener información sobre el ámbito.             |
| [**ITAttributeList**](itattributelist.md)                         | Permite obtener y establecer atributos sin interpretar.                                                                   |
| [**ITConferenceBlob**](itconferenceblob.md)                       | Proporciona acceso a información de conferencia específica del proveedor.                                                              |
| [**ITConnection**](itconnection.md)                               | Proporciona métodos para manipular factores de conexión, como la dirección de la conferencia, el ámbito y el ancho de banda.                       |
| [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)                                 | Obtiene y establece la información del directorio y proporciona acceso a un objeto de directorio determinado.                                |
| [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)                     | Obtiene y establece información genérica para una conferencia o un usuario dentro de un directorio.                                            |
| [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) | Obtiene y establece información genérica específica de una conferencia, como las horas de inicio y de detenerse.                                 |
| [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)             | Obtiene y establece información genérica específica de un usuario, como el nombre de un equipo que es el teléfono IP principal del usuario. |
| [**ITILSConfig**](/windows/desktop/api/Rend/nn-rend-itilsconfig)                                 | Obtiene y establece información específica del servidor de un directorio ILS determinado.                                                |
| [**ITMedia**](itmedia.md)                                         | Obtiene y establece las propiedades de medios básicas, como el nombre del medio y el protocolo de transporte.                                       |
| [**ITMediaCollection**](itmediacollection.md)                     | Permite el acceso multimedia por índice. Habilita la creación y eliminación de medios.                                                     |
| [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous)                               | Interfaz principal para el control Rendezvous.                                                                                |
| [**ITSdp**](itsdp.md)                                             | Manipula el blob SDP (Protocolo de descripción de sesión). Referencia: RFC 2327.                                             |
| [**ITTime**](ittime.md)                                           | Proporciona acceso a un conjunto de horas de activación para la sesión.                                                             |
| [**ITTimeCollection**](ittimecollection.md)                       | Permite el acceso de componente de tiempo por índice. Habilita la creación y eliminación de componentes de tiempo.                                  |



 

 

 



