---
title: Active Directory objetos de interfaces de servicio
description: El modelo de objetos ADSI consta de objetos COM. Los clientes manipulan objetos con interfaces. Los proveedores adsi implementan los objetos y sus interfaces.
ms.assetid: 3c9fd08e-47d6-4b71-8259-7c831d7d95c9
ms.tgt_platform: multiple
keywords:
- adsi de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20d75454b840597e1fd2ac0599d72d04acb1ee674f84aff40da64f9886879cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181195"
---
# <a name="active-directory-service-interfaces-objects"></a>Active Directory objetos de interfaces de servicio

El modelo de objetos ADSI consta de objetos COM. Los clientes manipulan objetos con interfaces. Los proveedores adsi implementan los objetos y sus interfaces.

Los objetos ADSI son objetos COM que representan un elemento dentro de un servicio de directorio: equipos, usuarios, archivos, servidores, impresoras, colas de impresión, entre otros. es decir, los elementos con los que trabajan diariamente los administradores de red. ADSI define diferentes tipos de objetos para representar diferentes tipos de elementos. Cada objeto, como se muestra en la ilustración siguiente, admite una o varias interfaces COM que permiten el acceso a los datos del objeto, a menudo denominados metadatos.

![Objetos de interfaces de servicio de Active Directory](images/ds2objex.png)

Dado que las interfaces COM son conjuntos de propiedades y métodos conectados lógicamente, puede pensar en cada interfaz como un identificador para el objeto que proporciona acceso a solo un conjunto de funciones lógicas a la vez. En la tabla siguiente se enumeran los elementos ADSI fundamentales.



| Interfaz            | Descripción                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iads**             | Se usa para la identificación de objetos. Como interfaz fundamental necesaria en todos los objetos ADSI, los [**IAD proporciona**](/windows/desktop/api/Iads/nn-iads-iads) acceso a los metadatos del objeto, incluida su definición en el esquema ADSI. Los IAD también proporcionan acceso a las propiedades y métodos que administran los datos de objetos en la caché de propiedades.                                                                                   |
| **IADsContainer**    | Se usa para la administración y detección de objetos. Todos los objetos de contenedor ADSI requieren la interfaz [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) para administrar la creación, eliminación, copia y movimiento de objetos, enlace y enumeración.                                                                                                                                                                      |
| **IADsPropertyList** | Se usa para la administración de propiedades de objetos. La [**interfaz IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) optimiza la administración de datos de objetos en la caché de propiedades.                                                                                                                                                                                                                                |
| **IDirectoryObject** | Se usa para el acceso directo a objetos. La [**interfaz IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) proporciona acceso a objetos de bajo nivel para los clientes que no usan Automation. Esta interfaz omite la caché de propiedades de objeto y proporciona acceso directo a las propiedades del objeto. Para obtener más información, [vea The IADs and IDirectoryObject Interfaces](the-iads-and-idirectoryobject-interfaces.md). |
| **IUnknown**         | Se usa para la administración de objetos COM. La [**interfaz IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) es necesaria para todos los objetos COM.                                                                                                                                                                                                                                                                              |
| **IDispatch**        | Se usa para la invocación de métodos y datos de la biblioteca de tipos. La [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) es necesaria para todos los objetos de Automation.                                                                                                                                                                                                                             |



 

Los objetos ADSI más complejos pueden exponer interfaces adicionales. Por ejemplo, [**IADsCollection admite métodos**](/windows/desktop/api/Iads/nn-iads-iadscollection) que administran colecciones de elementos de directorio del mismo tipo de datos. [**Los métodos IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) administran las colecciones de casos especiales de objetos que admiten la [**interfaz IADsMembers.**](/windows/desktop/api/Iads/nn-iads-iadsmembers) Para los proveedores que lo admiten, la [**interfaz IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) admite métodos para consultar servicios de directorio. Además, ADSI proporciona interfaces que representan elementos lógicos y físicos conocidos. Por ejemplo, los objetos ADSI que representan usuarios admiten [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), los que representan equipos admiten [**IADsComputer,**](/windows/desktop/api/Iads/nn-iads-iadscomputer)y así sucesivamente. Para obtener más información sobre los objetos ADSI, vea [The IADs and IDirectoryObject Interfaces](the-iads-and-idirectoryobject-interfaces.md). No todos los proveedores implementan todas las interfaces o todos los métodos y propiedades en todas las interfaces. Para obtener más información, vea [REFERENCIA DE ADSI.](adsi-reference.md)

 

 