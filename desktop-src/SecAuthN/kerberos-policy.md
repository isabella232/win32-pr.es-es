---
description: La directiva de vales de Kerberos se define en el nivel de dominio y se implementa mediante la directiva Centro de distribución de claves dominio (KDC).
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Directiva Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4559353e65a25a380c0c2aa4bb7e5d56f7681af1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073771"
---
# <a name="kerberos-policy"></a>Directiva Kerberos

La directiva de vales de Kerberos se define en el nivel de dominio y se implementa mediante el Centro de distribución de claves [*dominio*](../secgloss/k-gly.md) (KDC). La directiva kerberos se almacena en el Active Directory como un subconjunto de los atributos de la directiva de seguridad de dominio. De forma predeterminada, las opciones de directiva solo las pueden establecer los miembros del grupo Administradores de dominio. La directiva de dominio incluye opciones que:

-   Soporte técnico de vales posdados
-   Admitir la delegación restringida (solo Windows Server 2003)
-   Vales de soporte técnico que se pueden reenviar
-   Soporte técnico de vales para el sector energético
-   Establecer la antigüedad máxima del vale
-   Establecer la antigüedad máxima de renovación
-   Establecer la antigüedad máxima del vale de proxy
-   Cerrar la sesión forzada de los usuarios cuando expiren los vales

Con [*la delegación restringida,*](../secgloss/c-gly.md)se puede establecer un equipo para permitir el reenvío de credenciales solo a una lista específica de servicios. Esos servicios deben residir en el mismo dominio que el equipo que reenvía las credenciales. En *la delegación restringida,* los vales ya no se envían desde el cliente al servidor. El equipo servidor crea vales de servicio para reenviar según sea necesario a partir de la información utilizada para autenticar al cliente.

Aunque la directiva Kerberos para un dominio puede permitir la autenticación delegada al permitir el reenvío de vales, ese aspecto de la directiva no es necesario aplicar a todos los usuarios o a todos los equipos. Un atributo de una cuenta de usuario individual se puede establecer para deshabilitar el reenvío de las credenciales de ese usuario [*por*](../secgloss/c-gly.md) cualquier servidor. Se puede establecer un atributo de la cuenta de un equipo individual para deshabilitar el reenvío de credenciales de cualquier usuario. En ambos casos, la delegación se puede deshabilitar mediante la creación de una directiva de grupo que se aplique a todos los usuarios o a todos los equipos de una unidad organizativa de la Active Directory.

**Windows XP/2000:** No se admite la delegación restringida.

 

 
