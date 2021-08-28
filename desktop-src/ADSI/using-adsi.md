---
title: Uso de Active Directory interfaces de servicio
description: Active Directory Service Interfaces (ADSI) proporciona los medios para que las aplicaciones cliente de servicios de directorio usen un conjunto de interfaces para comunicarse con cualquier espacio de nombres que proporciona una implementación adsi.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Uso Active Directory ADSI de interfaces de servicio
- ADSI ADSI , Usar
- Active Directory interfaces de servicio ADSI , Using
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15495f9fa21f436570381ea8f0b2a7c7fff5f4efed645a5f3465a3b5d2929776
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648855"
---
# <a name="using-active-directory-service-interfaces"></a>Uso de Active Directory interfaces de servicio

Active Directory Service Interfaces (ADSI) proporciona los medios para que las aplicaciones cliente de servicios de directorio usen un conjunto de interfaces para comunicarse con cualquier espacio de nombres que proporciona una implementación adsi. Los clientes ADSI usan las interfaces de servicio de Active Directory bien definidas en lugar de las llamadas API específicas de la red para obtener un acceso más sencillo a los servicios de un espacio de nombres.

Active Directory service interfaces se ajustan al modelo de objetos componentes (COM) y admiten características COM estándar.

ADSI proporciona interfaces compatibles con Automation para controladores enlazados a nombres como Java, el sistema de desarrollo de Microsoft Visual Basic y Visual Basic Scripting Edition (VBScript). ADSI también puede proporcionar una interfaz que puede optimizar el rendimiento de las interfaces que no son compatibles con Automation, para usarlas con entornos de lenguaje como C y C++.

ADSI también proporciona las interfaces que no son de automatización, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch,**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)para admitir consultas y administración de objetos de directorio.

Además, ADSI proporciona su propio proveedor de OLE DB, para que cualquier cliente que ya use OLE DB, incluidos los que usan ActiveX Data Objects, pueda consultar directamente los servicios de directorio.

Las aplicaciones web que Active Server Pages también pueden programar el acceso a los servicios de directorio a través de ADSI.

Los clientes ADSI pueden detectar mediante programación todos los proveedores de ADSI en un sitio y usar las mismas interfaces para comunicarse con cada espacio de nombres. A medida que se instalan proveedores adicionales, los clientes ADSI también pueden comunicarse, sin volver a compilar, con los nuevos espacios de nombres.

En esta guía de programación se describe cómo funciona ADSI y se proporciona información para realizar tareas específicas en ADSI. Se tratan los temas siguientes:

-   [Enlace a un objeto ADSI](binding-to-an-adsi-object.md)
-   [Crear y eliminar objetos](creating-and-deleting-objects.md)
-   [Acceso y manipulación de datos con ADSI](accessing-and-manipulating-data-with-adsi.md)
-   [Uso del esquema ADSI](using-the-adsi-schema.md)
-   [Colecciones y grupos](collections-and-groups.md)
-   [Enumeración de objetos ADSI](enumerating-adsi-objects.md)
-   [Buscar Active Directory](searching-active-directory.md)
-   [Modelo de seguridad ADSI](adsi-security-model.md)
-   [Extensiones ADSI](adsi-extensions.md)
-   [Uso de ADSI con Exchange](using-adsi-with-exchange.md)
-   [Interfaces de utilidad ADSI](adsi-utility-interfaces.md)
-   [Programación de ADSI con Java/COM](programming-adsi-with-javacom.md)

 

 




