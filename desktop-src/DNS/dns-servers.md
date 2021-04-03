---
title: Servidores DNS
description: Un servidor DNS es un equipo que completa el proceso de resolución de nombres en DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- Servidores DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509ceeb811f221560540ae60f269c6ee1b05444f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777778"
---
# <a name="dns-servers"></a>Servidores DNS

Un *servidor DNS* es un equipo que completa el proceso de resolución de nombres en DNS. Los servidores DNS contienen [*archivos de zona*](z-gly.md) que les permiten resolver nombres en direcciones IP y direcciones IP en nombres. Cuando se consulta, un servidor DNS responderá de una de estas tres maneras:

-   El servidor devuelve los datos solicitados de resolución de nombres o resolución IP.
-   El servidor devuelve un puntero a otro servidor DNS que puede atender la solicitud.
-   El servidor indica que no tiene los datos solicitados.

Los servidores DNS podrían, durante el transcurso de la preparación de devolver los datos de resolución solicitados, consultar otros servidores DNS, pero más allá de eso, los servidores DNS no realizan ninguna otra operación.

Hay tres tipos principales de servidores DNS: los servidores principales, los servidores secundarios y los servidores de almacenamiento en caché.

## <a name="primary-server"></a>Servidor principal

El *servidor principal* es el servidor autoritativo para la zona. Todas las tareas administrativas asociadas a la zona (por ejemplo, la creación de subdominios dentro de la zona u otras tareas administrativas similares) deben realizarse en el servidor principal. Además, los cambios asociados a la zona o las modificaciones o adiciones a los RRs en los archivos de zona deben realizarse en el servidor principal. En el caso de una zona determinada, hay un servidor principal, excepto cuando se integra Active Directory Services y el servidor DNS de Microsoft.

## <a name="secondary-servers"></a>Servidores secundarios

*Los servidores secundarios* son servidores DNS de copia de seguridad. Los servidores secundarios reciben todos sus archivos de zona de los archivos de zona del servidor principal en una transferencia de zona. Pueden existir varios servidores secundarios para cualquier zona determinada, tanto como sea necesario para proporcionar [*equilibrio de carga*](l-gly.md), [*tolerancia a errores*](f-gly.md)y reducción del tráfico. Además, cualquier servidor DNS determinado puede ser un servidor secundario para varias zonas.

Además de los servidores DNS principal y secundario, se pueden usar roles de servidor DNS adicionales cuando dichos servidores sean adecuados para una infraestructura DNS. Estos servidores adicionales son servidores de almacenamiento en caché y [*reenviadores*](f-gly.md).

## <a name="caching-servers"></a>Servidores de almacenamiento en caché

[*Los servidores de almacenamiento en caché*](c-gly.md), también conocidos como servidores de solo almacenamiento en caché, realizan como su nombre sugiere; solo proporcionan el servicio de consulta en caché para las respuestas DNS. En lugar de mantener archivos de zona como otros servidores secundarios, los servidores DNS de almacenamiento en caché realizan consultas, almacenan en caché las respuestas y devuelven los resultados al cliente que realiza la consulta. La principal diferencia entre los servidores de almacenamiento en caché y otros servidores secundarios es que otros servidores secundarios mantienen archivos de zona (y realizan transferencias de zona cuando es adecuado, lo que genera tráfico de red asociado a la transferencia), no los servidores de almacenamiento en caché.

 

 




