---
title: Información general sobre las técnicas de Change Tracking
description: Hay varias maneras en las que los mecanismos de seguimiento de cambios pueden variar en el ámbito de los cambios de seguimiento. una aplicación puede realizar un seguimiento de los cambios en un único atributo de un solo objeto, en todos los objetos de un dominio, etc.
ms.assetid: 7359e851-61b7-420d-beb0-f7f33f79b007
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91fce20dc5e9fe8fe98937bb13885be577185e04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075110"
---
# <a name="overview-of-change-tracking-techniques"></a>Información general sobre las técnicas de Change Tracking

Hay varias maneras en las que los mecanismos de seguimiento de cambios pueden variar:

-   Ámbito de seguimiento de cambios: una aplicación puede realizar un seguimiento de los cambios en un único atributo de un solo objeto, en todos los objetos de un dominio, etc. Si el mecanismo coincide con los requisitos de la aplicación, la aplicación recibe un mínimo de datos irrelevantes y, por tanto, mejora el rendimiento.
-   Escala de tiempo: a una aplicación se le notifica cada cambio que se produce, o se le puede notificar el efecto neto de los cambios durante un período de minutos u horas.

    El procesamiento de datos menos oportunos puede ser más eficaz, ya que es posible que se contraigan varios cambios en uno. Por ejemplo, si un atributo cambia tres veces dentro de un intervalo de una hora, se notificará a una aplicación que ha notificado los cambios acumulados durante una hora solo un cambio de atributo, no tres.

    Al pensar en las escalas de tiempo, tenga en cuenta el efecto de la latencia de replicación. Una actualización que se origina en un controlador de dominio no se replica de forma instantánea a otro controlador de dominio. Requerir mucho mejor las escalas de tiempo de seguimiento de cambios que la latencia de replicación esperada a menudo no proporciona ninguna ventaja real a la aplicación.

-   Sondeo frente a notificación: con sondeo, una aplicación realiza periódicamente una solicitud a un controlador de dominio para recibir los datos de seguimiento de cambios. Con la notificación, el controlador de dominio envía cambios a la aplicación solo cuando se producen cambios.

    La sobrecarga del sondeo es obvia: la aplicación puede solicitar datos de seguimiento de cambios cuando no se ha producido nada significativo. La sobrecarga de la notificación es más sutil. El servidor debe mantener los datos sobre las solicitudes de notificación y debe consultar estos datos para decidir si enviar o no una notificación. Esto puede Agregar sobrecarga a las solicitudes de actualización normales.

-   Expresar el conocimiento de la aplicación: persistente frente a temporal: cada mecanismo de seguimiento de cambios debe incluir algún método para el servidor que contiene los datos a los que se hace un seguimiento para comprender el estado de conocimiento de la aplicación, de modo que la idea de "cambiar" esté bien definida. Por ejemplo, el estado de la aplicación puede expresarse como "actualizado con todos los cambios que se produjeron en el DC d antes de la hora t". Un mecanismo basado en esta manera de expresar el estado de conocimiento de una aplicación proporciona una manera eficaz de que la aplicación obtenga los cambios que se han producido después del tiempo especificado.

    Si la expresión del conocimiento de la aplicación se puede conservar, es decir, se almacena de forma recuperable, como en un archivo o base de datos, el reinicio de la aplicación requiere menos recursos que si no lo es. En el ejemplo anterior, la expresión de la información de la aplicación puede persistir grabando el DC d y el tiempo t. Algunos mecanismos de notificación de cambios no permiten conservar estos datos. El servidor y la aplicación deben sincronizarse con algún otro mecanismo cuando se inicia la aplicación. Esto supone un uso intensivo de los recursos si hay varios objetos implicados y puede implicar una programación compleja.

Utilice las técnicas siguientes para realizar el seguimiento de los cambios en Active Directory Domain Services:

-   Utilice el control notificación de cambios para iniciar una búsqueda asincrónica persistente de los cambios que coincidan con un filtro especificado. Para obtener más información, consulte [notificaciones de cambio en Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md).
-   Use una búsqueda de sincronización de directorios (DirSync) para recuperar los cambios que se han producido desde la última búsqueda de DirSync. Para obtener más información, consulte [sondear los cambios mediante el control DirSync](polling-for-changes-using-the-dirsync-control.md).
-   Utilice el atributo USNChanged para buscar objetos que han cambiado desde la búsqueda anterior. Para obtener más información, consulte [sondear los cambios con USNChanged](polling-for-changes-using-usnchanged.md).

El control de notificación de cambios está diseñado para aplicaciones o servicios que requieren una notificación razonablemente de los cambios poco frecuentes. Un ejemplo es un servicio o un programa que almacena los datos de configuración en el servidor de Active Directory y se debe notificar inmediatamente cuando se produce un cambio. Tenga en cuenta que existen limitaciones en el control de notificaciones.

-   La solicitud de notificaciones depende de la latencia de replicación y del lugar en el que se ha producido el cambio. Es posible que se le notifique cuando un cambio se replique en la réplica que está supervisando, pero el cambio puede haberse originado mucho antes en otra réplica.
-   El control está restringido a la supervisión de un solo objeto o de los elementos secundarios inmediatos de un contenedor. Las aplicaciones que deben supervisar varios contenedores o los objetos no relacionados pueden registrar hasta cinco solicitudes de notificación.
-   Si hay demasiados clientes escuchando los cambios que se producen con frecuencia, afectará al rendimiento del servidor. En general, las aplicaciones deben limitar el uso de este control por motivos de rendimiento en el servidor. Si no necesita conocer los cambios inmediatamente, puede ser mejor sondear periódicamente los cambios en lugar de usar la notificación de cambios.

Las técnicas de búsqueda DirSync y USNChanged están diseñadas para aplicaciones que mantienen la coherencia entre los datos del servidor de Active Directory y los datos correspondientes en otro almacenamiento. Estas técnicas las usan las aplicaciones que sondean periódicamente los cambios. La técnica DirSync se basa en un control de servidor LDAP que puede usar a través de las API ADSI o LDAP. Las desventajas del control DirSync son que solo se pueden usar en una cuenta con privilegios elevados, como un administrador de dominio. A continuación se muestra una lista de las limitaciones del control DirSync:

-   El control DirSync solo se puede usar en una cuenta con privilegios elevados, como un administrador de dominio.
-   El control DirSync solo puede supervisar un contexto de nomenclatura completo. No se puede limitar el ámbito de una búsqueda de DirSync para supervisar solo un subárbol, contenedor u objeto específico en un contexto de nomenclatura.

La técnica de USNChanged no tiene estas limitaciones, aunque es algo más complicado de usar que DirSync.

 

 




