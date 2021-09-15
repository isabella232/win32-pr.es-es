---
description: El Centro de distribución de claves (KDC) se implementa como un servicio de dominio. Usa el Active Directory como base de datos de cuenta y el catálogo global para dirigir referencias a los KDC en otros dominios.
ms.assetid: f2a7c87c-9be7-4fd8-8ecd-4edf1f2336ef
title: Centro de distribución de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f473fc3b84fed05e157fa700e7549f025979a90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476551"
---
# <a name="key-distribution-center"></a>Centro de distribución de claves

El Centro de distribución de claves (KDC) se implementa como un servicio de dominio. Usa el Active Directory como base de datos de cuenta y el catálogo global para dirigir referencias a los KDC en otros dominios.

Al igual que en otras implementaciones del [*protocolo Kerberos*](../secgloss/k-gly.md), el KDC es un único proceso que proporciona dos servicios:

-   Servicio de autenticación (AS)

    Este servicio emite vales de concesión de vales (TTP) para la conexión con el servicio de concesión de vales en su propio dominio o en cualquier dominio de confianza. Para que un cliente pueda solicitar un vale a otro equipo, debe solicitar un TGT al servicio de autenticación en el dominio de cuenta del cliente. El servicio de autenticación devuelve un TGT para el servicio de concesión de vales en el dominio del equipo de destino. El TGT se puede reutilizar hasta que expire, pero el primer acceso al servicio de concesión de vales de cualquier dominio siempre requiere un viaje al servicio de autenticación en el dominio de cuenta del cliente.

-   Ticket-Granting Service (TGS)

    Este servicio emite vales para la conexión a equipos en su propio dominio. Cuando los clientes desean acceder a un equipo, se pondrán en contacto con el servicio de concesión de vales en el dominio del equipo de destino, presentarán un TGT y le pedirán un vale para el equipo. El vale se puede reutilizar hasta que expire, pero el primer acceso a cualquier equipo siempre requiere un viaje al servicio de concesión de vales en el dominio de cuenta del equipo de destino.

El KDC de un dominio se encuentra en un controlador de dominio, como es el Active Directory del dominio. La autoridad de seguridad [*local*](../secgloss/l-gly.md) (LSA) del controlador de dominio inicia automáticamente ambos servicios y se ejecutan como parte del proceso de LSA. No se puede detener ningún servicio. Si el KDC no está disponible para los clientes de red, el Active Directory tampoco está disponible y el controlador de dominio ya no controla el dominio. El sistema garantiza la disponibilidad de estos y otros servicios de dominio al permitir que cada dominio tenga varios controladores de dominio, todos del mismo nivel. Cualquier controlador de dominio puede aceptar solicitudes de autenticación y solicitudes de concesión de vales dirigidas al KDC del dominio.

El [*nombre de entidad*](../secgloss/s-gly.md) de seguridad usado por el KDC en cualquier dominio es "krbtgt", como se especifica en RFC [4120](https://www.ietf.org/rfc/rfc4120.txt). Cuando se crea un nuevo dominio, se crea automáticamente una cuenta para esta entidad de seguridad. La cuenta no se puede eliminar ni se puede cambiar el nombre. El sistema asigna automáticamente un valor de contraseña aleatoria a la cuenta durante la creación del dominio. La contraseña de la cuenta del KDC se usa para derivar una clave criptográfica para cifrar y descifrar los TTP que emite. La contraseña de una cuenta de confianza de dominio se usa para derivar una clave entre dominios para cifrar los vales de referencia.

Todas las instancias del KDC dentro de un dominio usan la cuenta de dominio para la entidad de seguridad "krbtgt". Los clientes envían mensajes al KDC de un dominio incluyendo el nombre principal del servicio, "krbtgt" y el nombre del dominio. Ambos elementos de información también se usan en vales para identificar la autoridad emisora. Para obtener información sobre los formularios de nombres y las convenciones de direccionamiento, vea [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).

 

 
