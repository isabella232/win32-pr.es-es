---
title: Implementar Active Directory proveedores de interfaces de servicio
description: Active Directory interfaces de servicio (ADSI) son interfaces COM que contienen objetos de servicio de directorio para exponerlas a los clientes de servicios de directorio. Al proporcionar una implementación de ADSI, se expande la base de cliente al conjunto de aplicaciones cliente ADSI.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Implementar Active Directory proveedores de interfaces de servicio ADSI
- Implementación de los proveedores ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bdd0da406d9e65af898664e76b5e455540ebeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772949"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a>Implementar Active Directory proveedores de interfaces de servicio

Active Directory interfaces de servicio (ADSI) son interfaces COM que contienen objetos de servicio de directorio para exponerlas a los clientes de servicios de directorio. Al proporcionar una implementación de ADSI, se expande la base de cliente al conjunto de aplicaciones cliente ADSI.

Al igual que con cualquier implementación COM, puede escribir un proveedor ADSI en muchos idiomas. Las interfaces COM ADSI se definen como interfaces duales que permiten la resolución de nombres en tiempo de ejecución y en tiempo de compilación, y se pueden llamar mediante lenguajes compatibles con automatización como Visual Basic, Visual Basic Scripting Edition y también los lenguajes más conscientes del rendimiento y la eficacia, como C y C++. Los clientes ADSI también incluyen aplicaciones web que usan Active Server páginas y complementos de administración a través de Microsoft Management Console.

Dado que ADSI proporciona su propio proveedor de OLE DB, la implementación de las características de búsqueda definidas por [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) también permite que los clientes ADSI consulten datos en el servicio de directorio.

Todos los objetos de servicio de directorio se pueden representar mediante un objeto ADSI genérico compatible con [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). ADSI proporciona los bloques de creación necesarios para representar las características y los servicios de cualquier servicio de directorio.

Además, las meta-interfaces ADSI representan objetos comunes utilizados por los administradores de directorios. Las propiedades de las metainterfaces se asignan a las propiedades que admite el servicio de directorio. Los clientes ADSI que programan en las interfaces de servicio Active Directory obtienen acceso a su servicio de directorio en cuanto se instala el proveedor y se reinicia el sistema.

Si el servicio de directorio admite una representación de esquema, la compatibilidad con las interfaces de administración de esquemas hace que el espacio de nombres sea accesible directamente para los exploradores del servicio de directorio. Al publicar las características a través del esquema, los clientes pueden consultar el servicio de directorio en línea y aprovechar los servicios que ofrece. Debido a la disponibilidad del esquema en línea y a la ventaja de la interfaz COM, puede seguir haciendo que las nuevas características estén disponibles para el software cliente mientras se admiten las versiones de nivel inferior.

 

 




