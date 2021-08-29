---
title: Reservas, registros y enrutamiento de espacios de nombres
description: La reserva y el registro son las operaciones por las que la API del servidor HTTP proporciona acceso al espacio de nombres de dirección URL en un equipo.
ms.assetid: dc66960b-36cd-4c09-be0a-3aec9a8a25d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba6ad1e585487b03fa33448ddb99b6f1c7eaa779c56cd6fd1d07d4e73df2ea1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823175"
---
# <a name="namespace-reservations-registrations-and-routing"></a>Reservas, registros y enrutamiento de espacios de nombres

La reserva y el registro son las operaciones por las que la API del servidor HTTP proporciona acceso al espacio de nombres de dirección URL en un equipo. Las aplicaciones pueden registrarse para una parte del espacio de nombres de dirección URL con el fin de dar servicio a las solicitudes de los clientes HTTP. La aplicación registra un espacio de nombres con la API del servidor HTTP mediante la [**función HttpAddUrl.**](/windows/desktop/api/Http/nf-http-httpaddurl) La API del servidor HTTP agrega las direcciones URL a la cola de solicitudes de la aplicación y enruta las solicitudes a las aplicaciones en función de las direcciones URL de sus colas. Sin embargo, para que la aplicación pueda registrarse para recibir solicitudes de un espacio de nombres de dirección URL, el administrador del sistema debe realizar una reserva para esa dirección URL en nombre del usuario que ejecuta la aplicación. De forma predeterminada, el espacio de nombres está cerrado, es decir, solo el administrador puede registrar UrlPrefixes hasta que el administrador escriba una reserva.

Una reserva asigna de forma persistente una parte del espacio de nombres de dirección URL a usuarios individuales, lo que les permite reservar o "poseer" esa parte del espacio de nombres. Las reservas dan al usuario el derecho de registrarse en las solicitudes de servicio para el espacio de nombres. La API del servidor HTTP garantiza que los usuarios no registren direcciones URL de partes del espacio de nombres que no poseen. Para garantizar la seguridad del espacio de nombres, las ACL (Access Control list) se aplican a la parte del espacio de nombres reservada para cada usuario.

Los espacios de nombres reservados se identifican mediante cadenas de prefijo de dirección URL, con el mismo formato que los prefijos de dirección URL usados para los registros. Esto significa que todas las distintas categorías de especificador de host también están disponibles para las reservas.

Las reservas de espacios de nombres se conservan en los reinicios y los cambios tienen efecto dinámicamente, por lo que no es necesario detener y reiniciar la máquina.

Los siguientes conceptos se aclaran aún más a medida que se aplican al proceso de registro y reserva de espacios de nombres.

-   Registro. El registro es la operación por la que una aplicación indica interés en recibir solicitudes para un UrlPrefix especificado. La API para el registro de direcciones URL [**es HttpAddUrl.**](/windows/desktop/api/Http/nf-http-httpaddurl) El registro suele producirse durante el inicio de la aplicación y se debe realizar cada vez que se inicia la aplicación.
-   Enrutamiento. La API del servidor HTTP realiza el enrutamiento para determinar la aplicación a la que se va a enviar la solicitud, en función de la dirección [UrlPrefix](urlprefix-strings.md) que mejor coincida y que esté registrada o reservada. La operación de enrutamiento usa la información de registro y reserva.
-   Reserva. Reservation asigna una parte del espacio de nombres de dirección URL a uno o varios usuarios. Esta operación concede a los usuarios el derecho de registrarse para el espacio de nombres especificado. Se dice que un usuario para el que se reserva un espacio de nombres es "propietario" de esa parte del espacio de nombres de dirección URL. Las reservas de espacios de nombres se realizan normalmente durante la instalación de la aplicación y son una operación poco frecuente. Las reservas persisten en los reinicios de la máquina y requieren privilegios de administrador en la máquina o la propiedad con privilegios de delegación para crear o eliminar.
-   Delegación. Los privilegios de delegación permiten a un usuario que posee un espacio de nombres entregar la propiedad de un subárbol a otro usuario mediante una reserva posterior. El administrador del sistema concede privilegios de delegación a un usuario cuando se realiza la reserva. A uno o varios usuarios se les pueden asignar privilegios de delegación a un espacio de nombres.

 

 




