---
title: Información general de Change Tracking técnicas
description: Hay varias maneras en que los mecanismos de seguimiento de cambios pueden diferir ámbito para realizar el seguimiento de los cambios Una aplicación puede realizar un seguimiento de los cambios en un único atributo de un solo objeto, en todos los objetos de un dominio, y así sucesivamente.
ms.assetid: 7359e851-61b7-420d-beb0-f7f33f79b007
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036a16362a7f27da47fc086d8758b28619f34d1475c7bb911050deb20c86f08d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025513"
---
# <a name="overview-of-change-tracking-techniques"></a>Información general de Change Tracking técnicas

Hay varias maneras en que los mecanismos de seguimiento de cambios pueden diferir:

-   Ámbito para realizar el seguimiento de los cambios: una aplicación puede realizar un seguimiento de los cambios en un único atributo de un único objeto, en todos los objetos de un dominio, y así sucesivamente. Si el mecanismo coincide con los requisitos de la aplicación, la aplicación recibe un mínimo de datos irrelevantes y, por tanto, mejora el rendimiento.
-   Escalas de tiempo: se notifica a una aplicación cada cambio a medida que se produce o se le puede notificar el efecto neto de los cambios durante un período de minutos u horas.

    El procesamiento de datos menos a tiempo puede ser más eficaz, ya que se pueden contraer varios cambios en uno. Por ejemplo, si un atributo cambia tres veces en un intervalo de una hora, una aplicación notificada de los cambios acumulados durante una hora recibirá una notificación de solo un cambio de atributo, no tres.

    Al pensar en la escala de tiempo, tenga en cuenta el efecto de la latencia de replicación. Una actualización que se origina en un controlador de dominio no se replica al instante en otro controlador de dominio. Requerir una escala de tiempo de seguimiento de cambios mucho mejor que la latencia de replicación esperada a menudo no proporciona ninguna ventaja real a la aplicación.

-   Sondeo frente a notificación: con el sondeo, una aplicación realiza periódicamente una solicitud a un controlador de dominio para recibir datos de seguimiento de cambios. Con la notificación, el controlador de dominio envía los cambios a la aplicación solo cuando se producen cambios.

    La sobrecarga del sondeo es obvia: la aplicación puede solicitar datos de seguimiento de cambios cuando no se ha producido nada significativo. La sobrecarga de la notificación es más sutil. El servidor debe mantener los datos sobre las solicitudes de notificación y debe consultar estos datos para decidir si quiere enviar o no una notificación. Esto puede agregar sobrecarga a las solicitudes de actualización normales.

-   Expresar el conocimiento de la aplicación: persistente frente a temporal: cada mecanismo de seguimiento de cambios debe incluir algún método para que el servidor que mantiene los datos de los que se realiza el seguimiento comprenda el estado de conocimiento de la aplicación, de modo que la idea de "cambio" esté bien definida. Por ejemplo, el estado de conocimiento de la aplicación podría expresarse como "Actualizado con todos los cambios que se produjeron en el controlador de dominio d antes de la hora t". Un mecanismo basado en esta forma de expresar el estado de conocimiento de una aplicación proporcionaría una manera eficaz para que la aplicación obtenga los cambios que se han producido más tarde de un tiempo especificado.

    Si se puede conservar la expresión del conocimiento de la aplicación, es decir, almacenarse de forma recuperable, como en un archivo o base de datos, el reinicio de la aplicación consume menos recursos que si no es posible. En el ejemplo anterior, la expresión del conocimiento de la aplicación se puede conservar registrando el controlador de dominio d y la hora t. Algunos mecanismos de notificación de cambios no permiten que estos datos se conserven. El servidor y la aplicación deben sincronizarse con algún otro mecanismo cuando se inicia la aplicación. Esto consume muchos recursos si hay varios objetos implicados y puede implicar una programación compleja.

Use las técnicas siguientes para realizar un seguimiento de los cambios en Active Directory Domain Services:

-   Use el control de notificación de cambios para iniciar una búsqueda asincrónica persistente de cambios que coincidan con un filtro especificado. Para obtener más información, [vea Change Notifications in Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md).
-   Use una búsqueda de sincronización de directorios (DirSync) para recuperar los cambios que se han producido desde la búsqueda anterior de DirSync. Para obtener más información, [vea Sondeo de cambios mediante el control DirSync](polling-for-changes-using-the-dirsync-control.md).
-   Use el atributo USNChanged para buscar objetos que han cambiado desde la búsqueda anterior. Para obtener más información, [vea Sondear los cambios mediante USNChanged.](polling-for-changes-using-usnchanged.md)

El control de notificación de cambios está diseñado para aplicaciones o servicios que requieren una notificación razonablemente rápida de cambios poco frecuentes. Un ejemplo es un servicio o programa que almacena datos de configuración en el servidor Active Directory y se debe notificar rápidamente cuando se produce un cambio. Tenga en cuenta que hay limitaciones del control de notificación.

-   La rapidez de las notificaciones depende de la latencia de replicación y de dónde se produjo el cambio. Es posible que se le notifique rápidamente cuando un cambio se replica en la réplica que está supervisando, pero es posible que el cambio se haya originado mucho antes en alguna otra réplica.
-   El control está restringido a la supervisión de un único objeto o los secundarios inmediatos de un contenedor. Las aplicaciones que deben supervisar varios contenedores u objetos no relacionados pueden registrar hasta cinco solicitudes de notificación.
-   Si hay demasiados clientes que escuchan los cambios que se producen con frecuencia, afectará al rendimiento del servidor. En general, las aplicaciones deben limitar su uso de este control por motivos de rendimiento en el servidor. Si no necesita conocer los cambios inmediatamente, puede ser mejor sondear periódicamente los cambios en lugar de usar la notificación de cambios.

Las técnicas de búsqueda DirSync y USNChanged están diseñadas para aplicaciones que mantienen la coherencia entre los datos del servidor Active Directory y los datos correspondientes en algún otro almacenamiento. Estas técnicas las usan las aplicaciones que sondean periódicamente los cambios. La técnica DirSync se basa en un control de servidor LDAP que puede usar a través de LAS API ADSI o LDAP. Las desventajas del control DirSync son que solo lo puede usar una cuenta con privilegios elevados, como un administrador de dominio. A continuación se muestra una lista de las limitaciones del control DirSync:

-   El control DirSync solo lo puede usar una cuenta con privilegios elevados, como un administrador de dominio.
-   El control DirSync solo puede supervisar un contexto de nomenclatura completo. No se puede limitar el ámbito de una búsqueda de DirSync para supervisar solo un subárbol, contenedor u objeto específicos en un contexto de nomenclatura.

La técnica USNChanged no tiene estas limitaciones, aunque es algo más complicado de usar que DirSync.

 

 




