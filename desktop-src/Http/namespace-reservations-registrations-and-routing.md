---
title: Reservas de espacio de nombres, registros y enrutamiento
description: La reserva y el registro son las operaciones por las que la API del servidor HTTP proporciona acceso al espacio de nombres de la dirección URL en un equipo.
ms.assetid: dc66960b-36cd-4c09-be0a-3aec9a8a25d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00801629b5b778bb6c87a0bff615cb9d5618f57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357624"
---
# <a name="namespace-reservations-registrations-and-routing"></a>Reservas de espacio de nombres, registros y enrutamiento

La reserva y el registro son las operaciones por las que la API del servidor HTTP proporciona acceso al espacio de nombres de la dirección URL en un equipo. Las aplicaciones pueden registrarse para una parte del espacio de nombres de la dirección URL con el fin de atender las solicitudes de los clientes HTTP. La aplicación registra un espacio de nombres con la API del servidor HTTP mediante la función [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) . La API del servidor HTTP agrega las direcciones URL a la cola de solicitudes de la aplicación y enruta las solicitudes a las aplicaciones en función de las direcciones URL de sus colas. Sin embargo, antes de que la aplicación pueda registrarse para recibir solicitudes de un espacio de nombres URL, el administrador del sistema debe realizar una reserva para esa dirección URL en nombre del usuario que ejecuta la aplicación. De forma predeterminada, el espacio de nombres está cerrado, es decir, solo el administrador puede registrar UrlPrefixes hasta que el administrador escriba una reserva.

Una reserva asigna de forma persistente una parte del espacio de nombres de la dirección URL a usuarios individuales, lo que les permite reservar o "poseer" esa parte del espacio de nombres. Las reservas proporcionan al usuario el derecho a registrarse en las solicitudes de servicio para el espacio de nombres. La API del servidor HTTP garantiza que los usuarios no registran direcciones URL de partes del espacio de nombres que no son de su propiedad. Con el fin de garantizar la seguridad del espacio de nombres, las ACL (lista de Access Control) se aplican a la parte del espacio de nombres reservada para cada usuario.

Los espacios de nombres reservados se identifican mediante cadenas de prefijos de dirección URL, con un formato similar al de los prefijos de dirección URL que se usan para los registros. Esto significa que todas las categorías de especificador de host también están disponibles para las reservas.

Las reservas de espacio de nombres se conservan a lo largo de los reinicios y los cambios surten efecto de forma dinámica, por lo que no es necesario detener y reiniciar el equipo.

Los siguientes conceptos se aclaran aún más a medida que se aplican al proceso de registro y reserva de espacios de nombres.

-   Registro. El registro es la operación por la que una aplicación indica el interés en recibir solicitudes de un UrlPrefix especificado. La API para el registro de direcciones URL es [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl). Normalmente, el registro se produce durante el inicio de la aplicación y se debe realizar cada vez que se inicia la aplicación.
-   Automático. El enrutamiento se realiza mediante la API del servidor HTTP para determinar la aplicación a la que se va a enviar la solicitud, en función de las [UrlPrefix](urlprefix-strings.md) de coincidencia más adecuadas registradas o reservadas. La operación de enrutamiento hace uso de la información de registro y de reserva.
-   Movs. La reserva asigna una parte del espacio de nombres de la dirección URL a uno o varios usuarios. Esta operación proporciona a los usuarios el derecho a registrarse para el espacio de nombres especificado. Un usuario para el que se reserva un espacio de nombres se dice "posee" esa parte del espacio de nombres de la dirección URL. Las reservas de espacio de nombres normalmente se realizan durante la instalación de la aplicación y son una operación poco frecuente. Las reservas se conservan a lo largo del reinicio de la máquina y requieren privilegios de administrador en el equipo o la propiedad con privilegios de delegación para crear o eliminar.
-   Delegado. Los privilegios de delegación permiten a un usuario que posee un espacio de nombres entregar la propiedad de un subárbol a otro usuario mediante una reserva posterior. El administrador del sistema concede privilegios de delegación a un usuario cuando se realiza la reserva. A uno o varios usuarios se les pueden asignar privilegios de delegación a un espacio de nombres.

 

 




