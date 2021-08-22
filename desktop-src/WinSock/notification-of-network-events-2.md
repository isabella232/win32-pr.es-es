---
description: Una de las responsabilidades más importantes de un proveedor de servicios de transporte de datos es proporcionar indicaciones al cliente cuando se han producido determinados eventos de red.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Notificación de eventos de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6fb24f746cbb03860bbd28c1028d92d7865a29c44baedaf2c227cb48536cd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794765"
---
# <a name="notification-of-network-events"></a>Notificación de eventos de red

Una de las responsabilidades más importantes de un proveedor de servicios de transporte de datos es proporcionar indicaciones al cliente cuando se han producido determinados eventos de red. La lista de eventos de red definidos consta de lo siguiente:

-   **FD \_ CONNECT:** se ha completado una conexión a un host remoto o a una sesión de multidifusión.
-   **FD \_ ACCEPT:** un host remoto realiza una solicitud de conexión.
-   **FD \_ READ:** han llegado datos de red que están disponibles para leerse.
-   **FD \_ WRITE:** el espacio está disponible en los búferes del proveedor de servicios para que ahora se puedan enviar datos adicionales.
-   **FD \_ OOB:** los datos fuera de banda están disponibles para leerse.
-   **FD \_ CLOSE:** el host remoto ha cerrado la conexión.
-   **FD \_ QOS:** se ha producido un cambio en los niveles de QoS negociados.
-   **FD \_ GROUP \_ QOS:** reservado.
-   **FD \_ CAMBIO \_ DE \_ LA** INTERFAZ DE ENRUTAMIENTO: ha cambiado una interfaz local que se debe usar para llegar al destino especificado en LA INTERFAZ DE ENRUTAMIENTO DE **SIO \_ CHANGE \_ \_ IOCTL.**
-   **FD \_ ADDRESS \_ LIST \_ CHANGE:** la lista de direcciones locales a las que se puede enlazar la aplicación ha cambiado.

El conjunto de eventos de red enumerados anteriormente a veces se conoce como eventos **\_ FD XXX.** La indicación de la aparición de uno o varios de estos eventos de red se puede dar de varias maneras, en función de cómo solicite la notificación el cliente.

 

 



