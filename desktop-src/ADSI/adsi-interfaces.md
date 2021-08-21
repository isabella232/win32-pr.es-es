---
title: ADSI Interfaces
description: En este tema se describen las categorías usadas para las interfaces ADSI.
ms.assetid: 8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd
ms.tgt_platform: multiple
keywords:
- ADSI Interfaces ADSI
- ADSI ADSI, reference,interfaces
- interfaces ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75463a2b9ce70013482d2abee4f21ff786e7914cff0fefe691c562c4f39edb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023823"
---
# <a name="adsi-interfaces"></a>ADSI Interfaces

Active Directory Interfaces de servicio (ADSI) admite un amplio conjunto de interfaces que se pueden clasificar según las siguientes categorías:

-   [Núcleo.](core-interfaces.md) Estas interfaces proporcionan las funciones básicas de administración de objetos de objetos ADSI. Las funciones principales incluyen proporcionar un punto de entrada en un almacén de directorios, cargar propiedades en la caché de propiedades y confirmar cambios en el directorio subyacente.
-   [Esquema](schema-interfaces.md). Estas interfaces proporcionan métodos para administrar y extender el esquema de directorio.
-   [Caché de propiedades](property-cache-interfaces.md). Estas interfaces definen métodos para manipular propiedades en la caché de propiedades.
-   [Objeto persistente](persistent-object-interfaces.md). Estas interfaces manipulan datos persistentes en el espacio de nombres del servicio de directorio subyacente. Los objetos ADSI implementan estos tipos de interfaces para proporcionar acceso a sus datos persistentes, incluidas cuentas de usuario, recursos compartidos de archivos, jerarquías organizativas y listas de trabajos en una cola de impresión.
-   [Objeto dinámico](dynamic-object-interfaces.md). Estas interfaces funcionan con datos dinámicos en un servicio de directorio. Los objetos de directorio no representados en el servicio de directorio subyacente implementan estas interfaces. Algunos ejemplos de datos dinámicos son los comandos emitidos a través de una red.
-   [Seguridad](security-interfaces.md). Estas interfaces permiten a un cliente ADSI establecer sus credenciales en un servidor y usar características de seguridad que admite el servicio de directorio, como la lista de control de acceso o los descriptores de seguridad.
-   [Que no es de Automation.](non-automation-interfaces.md) Estas interfaces permiten a los clientes que no son de Automation (por ejemplo, aplicaciones de C/C++) acceso de baja sobrecarga a objetos de directorio al proporcionar acceso vtable a métodos para administrar y buscar objetos de servicio de directorio.
-   [Extensión](extension-interfaces.md). Estas interfaces permiten a los clientes ADSI ampliar las características de las clases ADSI existentes para ofrecer soluciones personalizadas a los servicios de directorio.
-   [Utilidad](utility-interfaces.md). Estas interfaces proporcionan funciones auxiliares avanzadas para administrar objetos ADSI.
-   [Tipo de datos](data-type-interfaces.md). Estas interfaces proporcionan métodos para acceder a los tipos de datos ADSI.

 

 




