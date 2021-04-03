---
description: El Centro de distribución de claves (KDC) se implementa como un servicio de dominio. Utiliza el Active Directory como su base de datos de cuentas y el catálogo global para dirigir las referencias a los KDC de otros dominios.
ms.assetid: f2a7c87c-9be7-4fd8-8ecd-4edf1f2336ef
title: Centro de distribución de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f473fc3b84fed05e157fa700e7549f025979a90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082772"
---
# <a name="key-distribution-center"></a>Centro de distribución de claves

El Centro de distribución de claves (KDC) se implementa como un servicio de dominio. Utiliza el Active Directory como su base de datos de cuentas y el catálogo global para dirigir las referencias a los KDC de otros dominios.

Como en otras implementaciones del [*protocolo Kerberos*](../secgloss/k-gly.md), el KDC es un proceso único que proporciona dos servicios:

-   Servicio de autenticación (AS)

    Este servicio emite vales de concesión de vales (TGT) para la conexión con el servicio de concesión de vales en su propio dominio o en cualquier dominio de confianza. Para que un cliente pueda solicitar un vale a otro equipo, debe solicitar un TGT al servicio de autenticación en el dominio de la cuenta del cliente. El servicio de autenticación devuelve un TGT para el servicio de concesión de vales en el dominio del equipo de destino. El TGT se puede volver a usar hasta que expire, pero el primer acceso al servicio de concesión de vales de un dominio requiere siempre un viaje al servicio de autenticación en el dominio de la cuenta del cliente.

-   Servicio Ticket-Granting (TGS)

    Este servicio emite vales para la conexión a equipos en su propio dominio. Cuando los clientes quieren tener acceso a un equipo, se pone en contacto con el servicio de concesión de vales en el dominio del equipo de destino, presentan un TGT y solicitan un vale para el equipo. El vale se puede volver a usar hasta que expire, pero el primer acceso a cualquier equipo requiere siempre un viaje al servicio de concesión de vales en el dominio de la cuenta del equipo de destino.

El KDC de un dominio se encuentra en un controlador de dominio, como es el Active Directory del dominio. Ambos servicios se inician automáticamente mediante la autoridad de [*seguridad local*](../secgloss/l-gly.md) (LSA) del controlador de dominio y se ejecutan como parte del proceso de la LSA. No se puede detener ningún servicio. Si el KDC no está disponible para los clientes de red, el Active Directory también está disponible, y el controlador de dominio ya no controla el dominio. El sistema garantiza la disponibilidad de estos y otros servicios de dominio, ya que permite que cada dominio tenga varios controladores de dominio, todos los elementos del mismo nivel. Cualquier controlador de dominio puede aceptar solicitudes de autenticación y solicitudes de concesión de vales dirigidas al KDC del dominio.

El nombre de la [*entidad de seguridad*](../secgloss/s-gly.md) que usa el KDC en cualquier dominio es "krbtgt", según se especifica en [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt). Cuando se crea un dominio nuevo, se crea automáticamente una cuenta para esta entidad de seguridad. No se puede eliminar la cuenta, ni se puede cambiar el nombre. El sistema asigna automáticamente un valor de contraseña aleatoria a la cuenta durante la creación del dominio. La contraseña de la cuenta del KDC se usa para derivar una clave criptográfica para cifrar y descifrar los TGT que emite. La contraseña de una cuenta de confianza de dominio se usa para derivar una clave entre dominios para cifrar los vales de referencia.

Todas las instancias del KDC dentro de un dominio utilizan la cuenta de dominio para la entidad de seguridad "krbtgt". Los clientes direccionan los mensajes al KDC de un dominio incluyendo el nombre principal del servicio, "krbtgt", y el nombre del dominio. Los dos elementos de información también se usan en los vales para identificar la autoridad emisora. Para obtener información sobre las formas de nombres y las convenciones de direccionamiento, consulte [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).

 

 
