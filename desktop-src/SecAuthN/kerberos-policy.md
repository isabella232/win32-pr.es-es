---
description: La Directiva de vales de Kerberos se define en el nivel de dominio y se implementa mediante el Centro de distribución de claves del dominio (KDC).
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Directiva Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4559353e65a25a380c0c2aa4bb7e5d56f7681af1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652727"
---
# <a name="kerberos-policy"></a>Directiva Kerberos

La Directiva de vales de Kerberos se define en el nivel de dominio y se implementa mediante el [*centro de distribución de claves*](../secgloss/k-gly.md) del dominio (KDC). La Directiva de Kerberos se almacena en el Active Directory como un subconjunto de los atributos de la Directiva de seguridad de dominio. De forma predeterminada, solo los miembros del grupo administradores de dominio pueden establecer las opciones de directiva. La Directiva de dominio incluye opciones que:

-   Admitir vales postfechados
-   Delegación restringida de compatibilidad (solo Windows Server 2003)
-   Vales de soporte técnico que se pueden reenviar
-   Compatibilidad con vales renovables
-   Establecer la antigüedad máxima del vale
-   Establecer antigüedad máxima de renovación
-   Establecer la antigüedad máxima del vale de proxy
-   Cerrar la sesión de los usuarios cuando expiren los vales

Con la [*delegación restringida*](../secgloss/c-gly.md), un equipo puede establecerse para permitir el reenvío de credenciales únicamente a una lista específica de servicios. Estos servicios deben residir en el mismo dominio que el equipo que reenvía las credenciales. En *delegación restringida*, los vales ya no se envían desde el cliente al servidor. El equipo servidor crea vales de servicio para reenviar según sea necesario a partir de la información usada para autenticar el cliente.

Aunque la Directiva de Kerberos para un dominio puede permitir la autenticación delegada al permitir que se reenvíen vales, ese aspecto de la Directiva no necesita aplicarse a todos los usuarios o a todos los equipos. Un atributo de una cuenta de usuario individual se puede establecer para deshabilitar el reenvío de [*las credenciales*](../secgloss/c-gly.md) de ese usuario en cualquier servidor. Se puede establecer un atributo de la cuenta de un equipo individual para deshabilitar el reenvío de credenciales de cualquier usuario. En ambos casos, la delegación se puede deshabilitar mediante la creación de una directiva de grupo para aplicarla a todos los usuarios o a todos los equipos de una unidad organizativa de la Active Directory.

**Windows XP/2000:** No se admite la delegación restringida.

 

 
