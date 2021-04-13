---
title: Interfaces ADSI
description: En este tema se describen las categorías utilizadas para las interfaces ADSI.
ms.assetid: 8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd
ms.tgt_platform: multiple
keywords:
- ADSI (interfaces ADSI)
- ADSI ADSI, referencia, interfaces
- interfaces ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2930292defa99301fb74f37c933a9af24b73f1fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418365"
---
# <a name="adsi-interfaces"></a>Interfaces ADSI

Active Directory interfaces de servicio (ADSI) admite un amplio conjunto de interfaces que se pueden clasificar según las siguientes categorías:

-   [Núcleo](core-interfaces.md). Estas interfaces proporcionan funciones básicas de administración de objetos de los objetos ADSI. Las funciones principales incluyen proporcionar un punto de entrada a un almacén de directorios, cargar propiedades en la caché de propiedades y confirmar cambios en el directorio subyacente.
-   [Esquema](schema-interfaces.md). Estas interfaces proporcionan métodos para administrar y extender el esquema de directorio.
-   [Caché de propiedades](property-cache-interfaces.md). Estas interfaces definen métodos para manipular propiedades en la caché de propiedades.
-   [Objeto persistente](persistent-object-interfaces.md). Estas interfaces manipulan los datos persistentes en el espacio de nombres del servicio de directorio subyacente. Los objetos ADSI implementan estos tipos de interfaces para proporcionar acceso a sus datos persistentes, como cuentas de usuario, recursos compartidos de archivos, jerarquías organizativas y listas de trabajos en una cola de impresión.
-   [Objeto dinámico](dynamic-object-interfaces.md). Estas interfaces funcionan con datos dinámicos en un servicio de directorio. Los objetos de directorio no representados en el servicio de directorio subyacente implementan estas interfaces. Entre los ejemplos de datos dinámicos se incluyen comandos emitidos a través de una red.
-   [Seguridad](security-interfaces.md). Estas interfaces permiten a un cliente ADSI establecer sus credenciales en un servidor y usar las características de seguridad que admite el servicio de directorio, como la lista de control de acceso o los descriptores de seguridad.
-   [No Automation](non-automation-interfaces.md). Estas interfaces permiten a los clientes que no son de automatización (por ejemplo, aplicaciones de C/C++) el acceso de baja sobrecarga a los objetos de directorio al proporcionar acceso de vtable a métodos para administrar y buscar objetos de servicio de directorio.
-   [Extensión](extension-interfaces.md). Estas interfaces permiten a los clientes ADSI extender las características de las clases ADSI existentes para ofrecer soluciones personalizadas a los servicios de directorio.
-   [Utilidad](utility-interfaces.md). Estas interfaces proporcionan funciones auxiliares avanzadas para administrar objetos ADSI.
-   [Tipo de datos](data-type-interfaces.md). Estas interfaces proporcionan métodos para tener acceso a los tipos de datos ADSI.

 

 




