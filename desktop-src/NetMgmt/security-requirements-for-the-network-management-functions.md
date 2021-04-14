---
title: Requisitos de seguridad de la función de administración de red
description: La llamada a algunas de las funciones de administración de red no requiere la pertenencia al grupo especial.
ms.assetid: 846a5b81-d5bf-4275-a898-38e6ba308b8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b0987509294f03b8737aae5e721abf5dbdd90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533423"
---
# <a name="network-management-function-security-requirements"></a>Requisitos de seguridad de la función de administración de red

La llamada a algunas de las funciones de administración de red no requiere la pertenencia al grupo especial. Otras funciones requieren que los usuarios tengan un nivel de privilegios específico para ejecutarse correctamente. Cuando sea aplicable, en la sección Comentarios de la página de referencia de una función se indica el nivel de privilegios que debe tener un usuario para ejecutar la función concreta.

Los requisitos de seguridad que se aplican a los controladores de dominio de Active Directory pueden diferir de los que se aplican a los servidores y las estaciones de trabajo.

Para obtener más información y una lista de las funciones afectadas, vea los temas siguientes:

-   [Requisitos de las funciones de administración de red en los controladores de dominio de Active Directory](requirements-for-network-management-functions-on-active-directory-domain-controllers.md)
-   [Requisitos para las funciones de administración de redes en servidores y estaciones de trabajo](requirements-for-network-management-functions-on-servers-and-workstations.md)

Para obtener más información sobre cómo controlar el acceso a los objetos protegibles, vea [Access Control](/windows/desktop/SecAuthZ/access-control), [privilegios](/windows/desktop/SecAuthZ/privileges)y [objetos protegibles](/windows/desktop/SecAuthZ/securable-objects).

Para obtener más información acerca de los descriptores de seguridad específicos que se usan durante las comprobaciones de acceso, vea la página de referencia de funciones individuales. Para obtener más información sobre cómo llamar a funciones que requieran privilegios de administrador, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).

 

 