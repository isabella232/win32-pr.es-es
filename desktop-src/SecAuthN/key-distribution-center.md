---
description: El Centro de distribución de claves (KDC) se implementa como un servicio de dominio. Usa la base de Active Directory como base de datos de cuenta y el catálogo global para dirigir referencias a los KDC de otros dominios.
ms.assetid: f2a7c87c-9be7-4fd8-8ecd-4edf1f2336ef
title: Centro de distribución de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eef410ccb9289d30507708dc35000e1c15d5d4c9998b28b33a2e51d1a15b1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013345"
---
# <a name="key-distribution-center"></a>Centro de distribución de claves

El Centro de distribución de claves (KDC) se implementa como un servicio de dominio. Usa la base de Active Directory como base de datos de cuenta y el catálogo global para dirigir referencias a los KDC de otros dominios.

Al igual que en otras implementaciones del [*protocolo Kerberos,*](../secgloss/k-gly.md)el KDC es un único proceso que proporciona dos servicios:

-   Servicio de autenticación (AS)

    Este servicio emite vales de concesión de vales (TTP) para la conexión con el servicio de concesión de vales en su propio dominio o en cualquier dominio de confianza. Para que un cliente pueda solicitar un vale a otro equipo, debe solicitar un TGT al servicio de autenticación en el dominio de cuenta del cliente. El servicio de autenticación devuelve un TGT para el servicio de concesión de vales en el dominio del equipo de destino. El TGT se puede reutilizar hasta que expire, pero el primer acceso al servicio de concesión de vales de cualquier dominio siempre requiere un viaje al servicio de autenticación en el dominio de cuenta del cliente.

-   Ticket-Granting Service (TGS)

    Este servicio emite vales para la conexión a equipos en su propio dominio. Cuando los clientes desean acceder a un equipo, se pondrán en contacto con el servicio de concesión de vales en el dominio del equipo de destino, presentarán un TGT y le pedirán un vale para el equipo. El vale se puede reutilizar hasta que expire, pero el primer acceso a cualquier equipo siempre requiere un viaje al servicio de concesión de vales en el dominio de cuenta del equipo de destino.

El KDC de un dominio se encuentra en un controlador de dominio, como es el Active Directory para el dominio. Ambos servicios se inician automáticamente por la autoridad de seguridad [*local*](../secgloss/l-gly.md) (LSA) del controlador de dominio y se ejecutan como parte del proceso de LSA. No se puede detener ningún servicio. Si el KDC no está disponible para los clientes de red, el Active Directory tampoco está disponible y el controlador de dominio ya no controla el dominio. El sistema garantiza la disponibilidad de estos y otros servicios de dominio al permitir que cada dominio tenga varios controladores de dominio, todos del mismo nivel. Cualquier controlador de dominio puede aceptar solicitudes de autenticación y solicitudes de concesión de vales dirigidas al KDC del dominio.

El [*nombre de entidad*](../secgloss/s-gly.md) de seguridad utilizado por el KDC en cualquier dominio es "krbtgt", tal como se especifica en RFC [4120](https://www.ietf.org/rfc/rfc4120.txt). Cuando se crea un nuevo dominio, se crea automáticamente una cuenta para esta entidad de seguridad. La cuenta no se puede eliminar ni se puede cambiar el nombre. El sistema asigna automáticamente un valor de contraseña aleatorio a la cuenta durante la creación del dominio. La contraseña de la cuenta del KDC se usa para derivar una clave criptográfica para cifrar y descifrar los TTP que emite. La contraseña de una cuenta de confianza de dominio se usa para derivar una clave entre dominios para cifrar los vales de referencia.

Todas las instancias del KDC dentro de un dominio usan la cuenta de dominio para la entidad de seguridad "krbtgt". Los clientes direcciona los mensajes al KDC de un dominio mediante la inclusión del nombre principal del servicio, "krbtgt" y el nombre del dominio. Ambos elementos de información también se usan en vales para identificar la autoridad emisora. Para obtener información sobre los formularios de nombre y las convenciones de direccionamiento, vea [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).

 

 
