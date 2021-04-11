---
description: Los dos (o más) descriptores que hacen referencia a un socket compartido se pueden usar de forma independiente en lo que respecta a la e/s.
ms.assetid: 25252552-4b62-441a-b564-e7f4a77cf68a
title: Instrucciones de precedencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c2086b2d640e2968c56082c2d8dfff99546fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154256"
---
# <a name="precedence-guidelines"></a>Instrucciones de precedencia

Los dos (o más) descriptores que hacen referencia a un socket compartido se pueden usar de forma independiente en lo que respecta a la e/s. Sin embargo, la interfaz de Windows Sockets no implementa ningún tipo de control de acceso, por lo que depende de los procesos implicados en la coordinación de las operaciones en un socket compartido. Un uso típico de los sockets compartidos es disponer de un proceso que sea responsable de la creación de sockets y de establecer conexiones a los sockets en otros procesos responsables del intercambio de información.

La directriz general para admitir varias operaciones pendientes en sockets compartidos es que se recomienda que un proveedor de servicios respete todas las operaciones simultáneas en los sockets compartidos, especialmente la operación más reciente en un objeto de socket. Si es necesario, esto puede ocurrir a costa de que se cancelen algunas de las operaciones anteriores pero todavía pendientes, que devolverán WSAEINTR en este caso.

 

 



