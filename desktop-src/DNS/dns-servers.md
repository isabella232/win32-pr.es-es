---
title: Servidores DNS
description: Obtenga información sobre los servidores DNS. Un servidor DNS es un equipo que completa el proceso de resolución de nombres en DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- Servidores DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f1eb0391d588431e082c69bcd19768c4047b1e4e24c64fbda251c11703a7eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131835"
---
# <a name="dns-servers"></a>Servidores DNS

Un *servidor DNS* es un equipo que completa el proceso de resolución de nombres en DNS. Los servidores DNS contienen [*archivos de zona*](z-gly.md) que les permiten resolver nombres en direcciones IP y direcciones IP en nombres. Cuando se consulta, un servidor DNS responderá de una de estas tres maneras:

-   El servidor devuelve los datos de resolución de nombres o resolución de IP solicitados.
-   El servidor devuelve un puntero a otro servidor DNS que puede dar servicio a la solicitud.
-   El servidor indica que no tiene los datos solicitados.

Los servidores DNS pueden, durante el transcurso de la preparación para devolver los datos de resolución solicitados, consultar otros servidores DNS, pero más allá de eso, los servidores DNS no realizan ninguna otra operación.

Hay tres tipos principales de servidores DNS: servidores principales, servidores secundarios y servidores de almacenamiento en caché.

## <a name="primary-server"></a>Servidor principal

El *servidor principal* es el servidor autoritativo de la zona. Todas las tareas administrativas asociadas a la zona (como la creación de subdominios dentro de la zona u otras tareas administrativas similares) deben realizarse en el servidor principal. Además, los cambios asociados a la zona o las modificaciones o adiciones a RR en los archivos de zona deben realizarse en el servidor principal. Para cualquier zona determinada, hay un servidor principal, excepto cuando se integran Active Directory servicios y Microsoft DNS Server.

## <a name="secondary-servers"></a>Servidores secundarios

*Los servidores secundarios son* servidores DNS de copia de seguridad. Los servidores secundarios reciben todos sus archivos de zona de los archivos de zona del servidor principal en una transferencia de zona. Pueden existir varios servidores secundarios para cualquier zona determinada, tantos como sea necesario para proporcionar equilibrio de [*carga,*](l-gly.md)tolerancia a errores y reducción del tráfico. [](f-gly.md) Además, cualquier servidor DNS determinado puede ser un servidor secundario para varias zonas.

Además de los servidores DNS principales y secundarios, se pueden usar roles de servidor DNS adicionales cuando estos servidores son adecuados para una infraestructura DNS. Estos servidores adicionales son servidores de almacenamiento en caché y [*reenviadores.*](f-gly.md)

## <a name="caching-servers"></a>Servidores de almacenamiento en caché

[*Los servidores de almacenamiento en*](c-gly.md)caché, también conocidos como servidores de solo almacenamiento en caché, se realizan como sugiere su nombre. proporcionan solo el servicio de consulta en caché para las respuestas DNS. En lugar de mantener archivos de zona como hacen otros servidores secundarios, los servidores DNS de almacenamiento en caché realizan consultas, almacenan en caché las respuestas y devuelven los resultados al cliente de consulta. La principal diferencia entre los servidores de almacenamiento en caché y otros servidores secundarios es que otros servidores secundarios mantienen archivos de zona (y hacen transferencias de zona cuando corresponda, generando así tráfico de red asociado a la transferencia), los servidores de almacenamiento en caché no lo hacen.

 

 




