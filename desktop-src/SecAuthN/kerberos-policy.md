---
description: La directiva de vales de Kerberos se define en el nivel de dominio y se implementa mediante el Centro de distribución de claves (KDC) del dominio.
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Directiva Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d1dd394c42028c70f560fcb7f83b42bab506fbd222f877857be362a450041
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127315"
---
# <a name="kerberos-policy"></a>Directiva Kerberos

La directiva de vales de Kerberos se define en [](../secgloss/k-gly.md) el nivel de dominio y se implementa mediante el Centro de distribución de claves (KDC) del dominio. La directiva kerberos se almacena en el Active Directory como un subconjunto de los atributos de la directiva de seguridad de dominio. De forma predeterminada, las opciones de directiva solo las pueden establecer los miembros del grupo Administradores de dominio. La directiva de dominio incluye opciones que:

-   Compatibilidad con vales postdados
-   Admitir la delegación restringida (solo Windows Server 2003)
-   Vales de soporte técnico que se pueden reenviar
-   Compatibilidad con vales de energía
-   Establecer la antigüedad máxima del vale
-   Establecer la antigüedad máxima de renovación
-   Establecer la antigüedad máxima del vale de proxy
-   Cerrar sesión forzadamente de los usuarios cuando expiran los vales

Con [*la delegación restringida,*](../secgloss/c-gly.md)se puede establecer un equipo para permitir el reenvío de credenciales solo a una lista específica de servicios. Esos servicios deben residir en el mismo dominio que el equipo que reenvía las credenciales. En *la delegación restringida,* los vales ya no se envían desde el cliente al servidor. El equipo servidor crea vales de servicio para reenviar según sea necesario a partir de la información utilizada para autenticar el cliente.

Aunque la directiva Kerberos para un dominio puede permitir la autenticación delegada al permitir el reenvío de vales, ese aspecto de la directiva no tiene que aplicarse a todos los usuarios ni a todos los equipos. Cualquier servidor puede establecer un atributo de una cuenta de usuario individual para deshabilitar el reenvío de las credenciales de [*ese*](../secgloss/c-gly.md) usuario. Se puede establecer un atributo de la cuenta de un equipo individual para deshabilitar el reenvío de credenciales de cualquier usuario. En ambos casos, la delegación se puede deshabilitar mediante la creación de una directiva de grupo que se aplique a todos los usuarios o a todos los equipos de una unidad organizativa de la Active Directory.

**Windows XP/2000:** No se admite la delegación restringida.

 

 
