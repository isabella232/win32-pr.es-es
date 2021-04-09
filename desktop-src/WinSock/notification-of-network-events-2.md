---
description: Una de las responsabilidades más importantes de un proveedor de servicios de transporte de datos es que proporciona indicaciones al cliente cuando se han producido determinados eventos de red.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Notificación de eventos de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090d3adda7d34c0fe49eb14936bc01bf20878b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907940"
---
# <a name="notification-of-network-events"></a>Notificación de eventos de red

Una de las responsabilidades más importantes de un proveedor de servicios de transporte de datos es que proporciona indicaciones al cliente cuando se han producido determinados eventos de red. La lista de eventos de red definidos consta de lo siguiente:

-   **FD \_ CONECTAR**: se ha completado una conexión a un host remoto o a una sesión de multidifusión.
-   **FD \_ ACEPTAR**: un host remoto está realizando una solicitud de conexión.
-   **FD \_ LECTURA**: los datos de red llegaron a estar disponibles para su lectura.
-   **FD \_ ESCRITURA**: el espacio está disponible en los búferes del proveedor de servicios para que ahora se puedan enviar datos adicionales.
-   **FD \_ OOB**: los datos fuera de banda están disponibles para su lectura.
-   **FD \_ CERRAR**: el host remoto ha cerrado la conexión.
-   **FD \_ QOS**: se ha producido un cambio en los niveles de QoS negociados.
-   **FD \_ \_QoS de grupo**: reservado.
-   **FD \_ \_ \_ Cambio** de la interfaz de enrutamiento: una interfaz local que se debe usar para alcanzar el destino especificado en la **interfaz de enrutamiento de SiO el cambio de \_ \_ \_ ioctl** ha cambiado.
-   **FD \_ \_ \_ Cambio** en la lista de direcciones: la lista de direcciones locales a la que se puede enlazar la aplicación ha cambiado.

El conjunto de eventos de red enumerados anteriormente se denomina a veces eventos **FD \_ XXX** . La indicación de que se produzcan uno o varios de estos eventos de red se puede proporcionar de varias maneras, dependiendo de cómo el cliente solicite la notificación.

 

 



