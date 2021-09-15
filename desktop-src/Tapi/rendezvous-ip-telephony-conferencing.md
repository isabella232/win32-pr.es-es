---
description: Los controles TAPI 3 Rendezvous permiten a un programador crear aplicaciones que pueden crear y detectar conferencias IP de multidifusión multimedia.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Conferencia de telefonía IP de encuentro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1cbfc3a1e07fdc245af0ae6b93277c90083a75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474691"
---
# <a name="rendezvous-ip-telephony-conferencing"></a>Conferencia de telefonía IP de encuentro

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

Los controles TAPI 3 Rendezvous permiten a un programador crear aplicaciones que pueden crear y detectar conferencias IP de multidifusión multimedia.

Componentes clave de Rendezvous:

[Los controles de](directory-controls.md) directorio son una abstracción de las listas de conferencias en un servidor ILS o NTDS.

[Los controles de blobs en](conference-blob-controls.md) conferencias representan información específica de la conferencia, como la hora de inicio y de detenerse. Se proporcionan interfaces especiales para blobs de protocolo SDP. Para obtener información detallada, vea RFC 2327 titulada "SDP: Protocolo de descripción de sesión". Una copia actual de esta RFC se puede encontrar mediante un motor de búsqueda de Internet.

[Las interfaces COM de multidifusión](multicast-com-interfaces.md) son contenedores COM para las funciones DE MADCAP, anteriormente conocidas como MDHCP. Estas interfaces permiten a una aplicación obtener direcciones de multidifusión de un servidor de asignación de direcciones de multidifusión.

En el siguiente material se proporciona información general y algunos ejemplos de uso de los controles Rendezvous para telefonía IP y conferencias.

 

 



