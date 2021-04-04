---
title: Acerca de las interfaces de usuario de Active Directory Domain Services
description: Los administradores y los usuarios deben poder ver y modificar objetos de servicio de directorio en Microsoft Active Directory Domain Services desde una interfaz de usuario.
ms.assetid: b6eec599-ebb3-40af-a4a2-059755285854
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c451a44660aaadbf0021ff57e675736b797d8f3e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077483"
---
# <a name="about-the-user-interfaces-of-active-directory-domain-services"></a>Acerca de las interfaces de usuario de Active Directory Domain Services

Los administradores y los usuarios deben poder ver y modificar objetos de servicio de directorio en Microsoft Active Directory Domain Services desde una interfaz de usuario. Los administradores administran el servidor de Active Directory mediante diferentes complementos de Microsoft Management Console (MMC), en concreto, el Active Directory Domain Services usuarios y equipos, Active Directory Domain Services sitios y servicios, Active Directory Domain Services dominios y confianzas y Active Directory Domain Services complementos del administrador de esquemas. El usuario final, si se le conceden los permisos adecuados, también puede usar el complemento MMC de Active Directory para ver los objetos de directorio. El shell de Windows también se puede usar para ver objetos de directorio. El shell de Windows permite a los usuarios examinar objetos almacenados en el directorio desde el elemento de directorio en mis sitios de red en el escritorio o a través de los cuadros de diálogo de búsqueda disponibles en el menú Inicio.

Active Directory Domain Services admiten una interfaz de usuario que se adapta para satisfacer las necesidades de los administradores y los usuarios finales. Active Directory Domain Services permiten extender la interfaz de usuario que representa las clases de objeto existentes, así como las nuevas clases que se agregan al esquema. Los elementos siguientes se pueden usar para controlar o extender la interfaz de usuario para cada clase definida en el esquema:

-   [Páginas de propiedades para su uso con especificadores de presentación](property-pages-for-use-with-display-specifiers.md)
-   [Menús contextuales para su uso con especificadores de presentación](context-menus-for-use-with-display-specifiers.md)
-   [Nombres para mostrar de clases y atributos](class-and-attribute-display-names.md)
-   [Asistentes para crear objetos](object-creation-wizards.md)
-   [Iconos de clase](class-icons.md)
-   [Ver contenedores como nodos de hoja](viewing-containers-as-leaf-nodes.md)

A partir de Windows 2000, el sistema proporciona objetos COM que implementan cuadros de diálogo comunes para trabajar con objetos de directorio. Estos cuadros de diálogo proporcionan una interfaz de usuario común sin tener que volver a implementar estos cuadros de diálogo.

-   [Selector de objetos de directorio](directory-object-picker.md)
-   [Explorador de dominio](domain-browser.md)
-   [Explorador de contenedor](container-browser.md)

Active Directory complementos administrativos, los menús contextuales y las páginas de propiedades se pueden extender mediante los complementos de extensión MMC. También se pueden implementar otras extensiones de MMC, como cuadros de herramientas, elementos de espacio de nombres, barras de control y barras de herramientas. Para obtener más información, consulte [extensión de los complementos administrativos de Active Directory](/previous-versions/windows/desktop/mmc/extending-the-active-directory-administrative-snap-ins).

 

 