---
description: Los controles TAPI 3 Rendezvous permiten a un programador crear aplicaciones que pueden crear y detectar conferencias IP de multidifusión multimedia.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Rendezvous IP Telephony Conferencing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c1486f2ca730f1efb0391fdea5a3ad22bec65385a31bce9bf233f0f230b7ee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773575"
---
# <a name="rendezvous-ip-telephony-conferencing"></a>Rendezvous IP Telephony Conferencing

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

Los controles TAPI 3 Rendezvous permiten a un programador crear aplicaciones que pueden crear y detectar conferencias IP de multidifusión multimedia.

Componentes clave de Rendezvous:

[Los controles de](directory-controls.md) directorio son una abstracción de listas de conferencias en un servidor ILS o NTDS.

[Los controles de blobs de](conference-blob-controls.md) conferencia representan información específica de la conferencia, como la hora de inicio y de detenerse. Se proporcionan interfaces especiales para blobs de protocolo SDP. Para obtener información detallada, vea RFC 2327 titulada "SDP: Protocolo de descripción de sesión". Una copia actual de esta RFC se puede encontrar mediante un motor de búsqueda de Internet.

[Las interfaces COM de multidifusión](multicast-com-interfaces.md) son contenedores COM para las funciones DE MADCAP, anteriormente conocidas como MDHCP. Estas interfaces permiten a una aplicación obtener direcciones de multidifusión de un servidor de asignación de direcciones de multidifusión.

El siguiente material proporciona información general y algunos ejemplos de uso de los controles Rendezvous para la telefonía IP y la conferencia.

 

 



