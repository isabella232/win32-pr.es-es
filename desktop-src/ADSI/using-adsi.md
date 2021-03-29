---
title: Uso de interfaces de servicio Active Directory
description: Active Directory interfaces de servicio (ADSI) proporciona el medio para que las aplicaciones cliente de servicios de directorio utilicen un conjunto de interfaces para comunicarse con cualquier espacio de nombres que proporcione una implementación de ADSI.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Usar interfaces de servicio de Active Directory ADSI
- ADSI ADSI, usar
- Interfaces de servicio de Active Directory ADSI, usar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e500044ec755c393f8c8287528fee7f935751fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903019"
---
# <a name="using-active-directory-service-interfaces"></a>Uso de interfaces de servicio Active Directory

Active Directory interfaces de servicio (ADSI) proporciona el medio para que las aplicaciones cliente de servicios de directorio utilicen un conjunto de interfaces para comunicarse con cualquier espacio de nombres que proporcione una implementación de ADSI. Los clientes ADSI usan las interfaces de servicio Active Directory bien definidas en lugar de las llamadas API específicas de la red para obtener acceso más sencillo a los servicios de un espacio de nombres.

Active Directory interfaces de servicio se ajustan al modelo de objetos componentes (COM) y son compatibles con las características COM estándar.

ADSI proporciona interfaces que son compatibles con la automatización para controladores enlazados a nombres como Java, Microsoft Visual Basic Development System y Visual Basic Scripting Edition (VBScript). ADSI también puede proporcionar una interfaz que puede optimizar el rendimiento de las interfaces que no son compatibles con la automatización, para usarlas con entornos de lenguaje como C y C++.

ADSI también proporciona las interfaces que no son de automatización, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) y [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), para admitir las consultas y la administración de objetos de directorio.

Además, ADSI proporciona su propio proveedor de OLE DB, por lo que cualquier cliente que ya use OLE DB, incluidos los que usan Objetos de datos ActiveX, puede consultar directamente los servicios de directorio.

Las aplicaciones web que usan páginas de Active Server también pueden programar el acceso a los servicios de directorio a través de ADSI.

Los clientes ADSI pueden detectar mediante programación todos los proveedores ADSI en un sitio y utilizar las mismas interfaces para comunicarse con cada espacio de nombres. A medida que se instalan proveedores adicionales, los clientes ADSI pueden comunicarse, sin volver a compilar, también con los nuevos espacios de nombres.

Esta guía de programación describe cómo funciona ADSI y proporciona información para realizar tareas específicas en ADSI. Se tratan los temas siguientes:

-   [Enlazar a un objeto ADSI](binding-to-an-adsi-object.md)
-   [Crear y eliminar objetos](creating-and-deleting-objects.md)
-   [Obtener acceso a los datos y manipularlos con ADSI](accessing-and-manipulating-data-with-adsi.md)
-   [Usar el esquema ADSI](using-the-adsi-schema.md)
-   [Colecciones y grupos](collections-and-groups.md)
-   [Enumerar objetos ADSI](enumerating-adsi-objects.md)
-   [Buscar Active Directory](searching-active-directory.md)
-   [Modelo de seguridad ADSI](adsi-security-model.md)
-   [Extensiones ADSI](adsi-extensions.md)
-   [Usar ADSI con Exchange](using-adsi-with-exchange.md)
-   [Interfaces de la utilidad ADSI](adsi-utility-interfaces.md)
-   [Programar ADSI con Java/COM](programming-adsi-with-javacom.md)

 

 




