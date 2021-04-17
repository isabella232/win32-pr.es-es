---
description: En la tabla siguiente se enumeran los objetos COM y las interfaces asociadas a los controles de conferencias Rendezvous.
ms.assetid: d9634586-8315-46d3-9ffc-bfa9a4d7738e
title: Interfaces COM Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6df7fbdac45480ae7aa9d5968209f22fabe9a4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687504"
---
# <a name="rendezvous-com-interfaces"></a>Interfaces COM Rendezvous

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

En la tabla siguiente se enumeran los objetos COM y las interfaces asociadas a los controles de conferencias Rendezvous.

Para obtener más información sobre el modelo de objetos componentes (COM), consulte las secciones correspondientes en el kit de desarrollo de software (SDK) de la plataforma.



| Interfaces                                                         | Descripción                                                                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**IEnumDialableAddrs**](/windows/desktop/api/Rend/nn-rend-ienumdialableaddrs)                   | Enumera las direcciones marcables disponibles en el directorio actual.                                                     |
| [**IEnumDirectory**](/windows/desktop/api/Rend/nn-rend-ienumdirectory)                           | Enumera los objetos [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) .                                                                    |
| [**IEnumDirectoryObject**](/windows/desktop/api/Rend/nn-rend-ienumdirectoryobject)               | Enumera los objetos [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) .                                                        |
| [**IEnumMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)                         | Enumera los objetos [**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope) .                                                                    |
| [**IEnumMedia**](ienummedia.md)                                   | Enumera los objetos [**ITMedia**](itmedia.md) .                                                                            |
| [**IEnumTime**](ienumtime.md)                                     | Enumera los objetos [**ITTime**](ittime.md) .                                                                              |
| [**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)         | Interfaz principal para el contenedor COM de la asignación de direcciones de multidifusión.                                                           |
| [**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)                         | Proporciona métodos para recuperar y establecer la información de concesión de direcciones.                                                           |
| [**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)                                 | Encapsula todas las propiedades de un ámbito de multidifusión y proporciona métodos para obtener información sobre el ámbito.             |
| [**ITAttributeList**](itattributelist.md)                         | Permite obtener y establecer los atributos no interpretados.                                                                   |
| [**ITConferenceBlob**](itconferenceblob.md)                       | Proporciona acceso a la información de conferencia específica del proveedor.                                                              |
| [**ITConnection**](itconnection.md)                               | Proporciona métodos para manipular factores de conexión, como la dirección de la Conferencia, el ámbito y el ancho de banda.                       |
| [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)                                 | Obtiene y establece la información de directorio y proporciona acceso a un objeto de directorio determinado.                                |
| [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)                     | Obtiene y establece información genérica para una conferencia o un usuario dentro de un directorio.                                            |
| [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) | Obtiene y establece la información genérica específica de una conferencia, como las horas de inicio y detención.                                 |
| [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)             | Obtiene y establece la información genérica específica de un usuario, como el nombre de un equipo que es el teléfono IP principal del usuario. |
| [**ITILSConfig**](/windows/desktop/api/Rend/nn-rend-itilsconfig)                                 | Obtiene y establece información específica del servidor de un directorio ILS determinado.                                                |
| [**ITMedia**](itmedia.md)                                         | Obtiene y establece propiedades multimedia básicas como el nombre del medio y el protocolo de transporte.                                       |
| [**ITMediaCollection**](itmediacollection.md)                     | Permite el acceso a los medios por índice. Habilita la creación y eliminación de elementos multimedia.                                                     |
| [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous)                               | Interfaz principal del control Rendezvous.                                                                                |
| [**ITSdp**](itsdp.md)                                             | Manipula el BLOB SDP (Protocolo de descripción de la sesión). Referencia: RFC 2327.                                             |
| [**ITTime**](ittime.md)                                           | Proporciona acceso a un conjunto de tiempos de activación para la sesión.                                                             |
| [**ITTimeCollection**](ittimecollection.md)                       | Permite el acceso de los componentes de tiempo por índice. Habilita la creación y la eliminación de componentes de hora.                                  |



 

 

 



