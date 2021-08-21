---
title: Implementación de Active Directory de interfaces de servicio
description: Active Directory interfaces de servicio (ADSI) son interfaces COM que encapsulan objetos de servicio de directorio para exponerlos a clientes de servicios de directorio. Al proporcionar una implementación de ADSI, se expande la base de cliente al conjunto de aplicaciones cliente adsi.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Implementación de Active Directory ADSI de proveedores de interfaces de servicio
- Implementación de ADSI Providers ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd3eb1275398a82a2ef179678e56cb9a7eda2e63eb4278906fc925fcb1d7cf6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427572"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a>Implementación de Active Directory de interfaces de servicio

Active Directory interfaces de servicio (ADSI) son interfaces COM que encapsulan objetos de servicio de directorio para exponerlos a clientes de servicios de directorio. Al proporcionar una implementación de ADSI, se expande la base de cliente al conjunto de aplicaciones cliente adsi.

Al igual que con cualquier implementación com, puede escribir un proveedor adsi en muchos idiomas. Las interfaces COM adsi se definen como interfaces duales que permiten la resolución de nombres en tiempo de ejecución y en tiempo de compilación y se pueden llamar mediante lenguajes compatibles con Automation, como Visual Basic, Visual Basic Scripting Edition, y también los lenguajes con mayor rendimiento y eficiencia, como C y C++. Los clientes ADSI también incluyen aplicaciones web que usan Active Server Pages y complementos de administración a través del Microsoft Management Console.

Dado que ADSI proporciona su propio proveedor de OLE DB, la implementación de las características de búsqueda definidas por [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) también permite a los clientes adsi consultar datos en el servicio de directorio.

Todos los objetos de servicio de directorio se pueden representar a través de un objeto ADSI genérico que admita [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). ADSI proporciona los bloques de creación necesarios para representar las características y servicios de cualquier servicio de directorio.

Además, las meta interfaces ADSI representan objetos comunes que usan los administradores de directorios. Las propiedades de las meta interfaces se asignan a las propiedades admitidas por el servicio de directorio. Los clientes ADSI que programan a Active Directory Service Interfaces obtienen acceso al servicio de directorio en cuanto se instala el proveedor y se reinicia el sistema.

Si el servicio de directorio admite una representación de esquema, la compatibilidad con las interfaces de administración de esquemas hace que el espacio de nombres sea accesible directamente para los exploradores del servicio de directorio. Al publicar las características a través del esquema, los clientes pueden consultar el servicio de directorio en línea y aprovechar los servicios que ofrece. Debido a la disponibilidad del esquema en línea y a la ventaja de la interfaz COM, puede seguir haciendo que las nuevas características estén disponibles para el software cliente mientras admite versiones de nivel inferior.

 

 




