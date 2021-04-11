---
description: Los controles de encuentro TAPI 3 permiten a los programadores crear aplicaciones que pueden crear y detectar conferencias IP de multidifusión multimedia.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Conferencias de telefonía IP de encuentro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1cbfc3a1e07fdc245af0ae6b93277c90083a75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276795"
---
# <a name="rendezvous-ip-telephony-conferencing"></a>Conferencias de telefonía IP de encuentro

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

Los controles de encuentro TAPI 3 permiten a los programadores crear aplicaciones que pueden crear y detectar conferencias IP de multidifusión multimedia.

Los componentes clave de Rendezvous:

[Los controles de directorio](directory-controls.md) son una abstracción de las listas de conferencias en un servidor ILS o Ntds.

[Los controles de BLOB de conferencia](conference-blob-controls.md) representan información específica de la Conferencia, como la hora de inicio y de finalización. Se proporcionan interfaces especiales para los blobs de protocolo SDP. Para obtener información detallada, consulte RFC 2327 titulado "SDP: Protocolo de descripción de la sesión". Se puede encontrar una copia actual de esta RFC mediante un motor de búsqueda de Internet.

Las [interfaces com multidifusión](multicast-com-interfaces.md) son contenedores com para las funciones MADCAP, anteriormente conocido como MDHCP. Estas interfaces permiten a una aplicación obtener direcciones de multidifusión de un servidor de asignación de direcciones de multidifusión.

En el material siguiente se proporciona información general y algunos ejemplos de uso de los controles Rendezvous para telefonía IP y conferencias.

 

 



