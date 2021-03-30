---
title: Uso de la extensión ADSI para Servicios de Escritorio remoto la configuración de usuario
description: La administración de propiedades de usuario específicas de Servicios de Escritorio remoto es posible mediante el uso de los métodos implementados por la extensión de interfaces de servicio Active Directory (ADSI), que se incluye con la biblioteca de vínculos dinámicos Tsuserex.dll.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto, uso de la extensión ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f115fecf1cce5c518e93206402f76e077109611
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995560"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a>Uso de la extensión ADSI para Servicios de Escritorio remoto la configuración de usuario

La extensión de interfaces de servicios de Active Directory (ADSI) para Servicios de Escritorio remoto configuración de usuario es una biblioteca que se incluye en la biblioteca de vínculos dinámicos Tsuserex.dll. La administración de propiedades de usuario específicas de Servicios de Escritorio remoto es posible mediante los métodos implementados por la extensión. Los métodos permiten la configuración de las propiedades que están disponibles en la interfaz de extensión para Servicios de Escritorio remoto usuarios.

La extensión ADSI para Servicios de Escritorio remoto configuración de usuario admite el examen y la manipulación de Servicios de Escritorio remoto propiedades de usuario almacenadas en la base de datos del servicio de directorio. La extensión también admite la configuración de las propiedades de usuario que se almacenan en el Active Directory, a través de la API del Protocolo ligero de acceso a directorios (LDAP).

El proveedor implementa los métodos siguientes:

-   [**IADs:: get**](/windows/desktop/api/iads/nf-iads-iads-get). Este método busca una propiedad concreta o un conjunto de propiedades en una instancia de la clase.
-   [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put). Este método configura una propiedad concreta o un conjunto de propiedades en una instancia de la clase.

Consulte la [referencia de la extensión ADSI para servicios de escritorio remoto configuración de usuario](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) para obtener una lista de las propiedades de usuario servicios de escritorio remoto específicas que se pueden configurar.

Para obtener más información sobre el acceso y la modificación de atributos con ADSI, vea [obtener acceso a datos y manipularlos con ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).

Para obtener más información sobre el uso de las convenciones de nomenclatura ADSI y las cadenas AdsPath, consulte la información sobre [proveedores de servicios ADSI](/windows/desktop/ADSI/adsi-system-providers) individuales en la documentación del kit de desarrollo de software (SDK) de las [interfaces de servicio de Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) .

 

 