---
title: Uso de la extensión ADSI para la Servicios de Escritorio remoto usuario
description: La administración de propiedades de usuario específicas de Servicios de Escritorio remoto es posible mediante los métodos implementados por la extensión Active Directory Service Interfaces (ADSI), que se empaqueta con la biblioteca de vínculos dinámicos Tsuserex.dll.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto , mediante la extensión ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe63a725531c21b64ed0ac10abdeb4f710465532ab95f7c416c88f6142f1d55e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423695"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a>Uso de la extensión ADSI para la Servicios de Escritorio remoto usuario

La Active Directory interfaces de servicio (ADSI) para la configuración de usuario de Servicios de Escritorio remoto es una biblioteca que se empaqueta con la biblioteca de vínculos dinámicos Tsuserex.dll. La administración Servicios de Escritorio remoto propiedades de usuario específicas del usuario es posible mediante los métodos implementados por la extensión . Los métodos permiten la configuración de las propiedades que están disponibles en la interfaz de extensión para Servicios de Escritorio remoto usuarios.

La extensión ADSI para Servicios de Escritorio remoto usuario admite el examen y la manipulación de Servicios de Escritorio remoto de usuario almacenadas en la base de datos del servicio de directorio. La extensión también admite la configuración de propiedades de usuario que se almacenan en el Active Directory, a través de la API del Protocolo ligero de acceso a directorios (LDAP).

El proveedor implementa los métodos siguientes:

-   [**IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get). Este método busca una propiedad específica o un conjunto de propiedades en una instancia de la clase .
-   [**IADs::P ut**](/windows/desktop/api/iads/nf-iads-iads-put). Este método configura una propiedad específica o un conjunto de propiedades en una instancia de la clase .

Consulte la [Referencia de la extensión ADSI](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) para Servicios de Escritorio remoto configuración de usuario para obtener una lista de las propiedades de usuario de Servicios de Escritorio remoto específicas que puede configurar.

Para obtener más información sobre el acceso y la modificación de atributos con ADSI, vea [Acceso y manipulación de datos con ADSI.](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi)

Para más información sobre el uso de convenciones de nomenclatura ADSI y cadenas AdsPath, consulte la información sobre los proveedores de servicios [ADSI](/windows/desktop/ADSI/adsi-system-providers) individuales en la documentación del Kit de desarrollo de software (SDK) de la plataforma de interfaces de servicio (SDK) de [Active Directory.](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)

 

 