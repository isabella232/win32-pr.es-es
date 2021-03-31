---
title: Active Directory objetos de interfaces de servicio
description: El modelo de objetos ADSI consta de objetos COM. Los clientes manipulan objetos con interfaces. Los proveedores ADSI implementan los objetos y sus interfaces.
ms.assetid: 3c9fd08e-47d6-4b71-8259-7c831d7d95c9
ms.tgt_platform: multiple
keywords:
- objetos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e356d9b1212b448d16bb6bba081f6141a877b0b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904819"
---
# <a name="active-directory-service-interfaces-objects"></a>Active Directory objetos de interfaces de servicio

El modelo de objetos ADSI consta de objetos COM. Los clientes manipulan objetos con interfaces. Los proveedores ADSI implementan los objetos y sus interfaces.

Los objetos ADSI son objetos COM que representan un elemento dentro de un servicio de directorio: equipos, usuarios, archivos, servidores, impresoras, colas de impresión, etc. es decir, los elementos que los administradores de red trabajan con diariamente. ADSI define diferentes tipos de objetos para representar diferentes tipos de elementos. Cada objeto, como se muestra en la siguiente ilustración, admite una o más interfaces COM que permiten el acceso a los datos de objeto, a menudo denominados metadatos.

![objetos de interfaces del servicio de Active Directory](images/ds2objex.png)

Dado que las interfaces COM son conjuntos de propiedades y métodos conectados lógicamente, puede pensar en cada interfaz como un identificador del objeto que proporciona acceso a un solo conjunto de funciones lógicas a la vez. En la tabla siguiente se enumeran los elementos ADSI fundamentales.



| Interfaz            | Descripción                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IADs**             | Se utiliza para la identificación de objetos. Como la interfaz fundamental necesaria en todos los objetos ADSI, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) proporciona acceso a los metadatos del objeto, incluida su definición en el esquema ADSI. IADs también proporciona acceso a las propiedades y los métodos que administran los datos de objeto en la memoria caché de propiedades.                                                                                   |
| **IADsContainer**    | Se usa para la administración y detección de objetos. Todos los objetos del contenedor ADSI requieren la interfaz [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) para administrar la creación, eliminación, copia y movimiento, enlace y enumeración de objetos.                                                                                                                                                                      |
| **IADsPropertyList** | Se usa para la administración de propiedades de objeto. La interfaz [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) optimiza la administración de datos de objetos en la memoria caché de propiedades.                                                                                                                                                                                                                                |
| **IDirectoryObject** | Se usa para el acceso directo a objetos. La interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) proporciona acceso a objetos de bajo nivel para los clientes que no usan la automatización. Esta interfaz omite la memoria caché de propiedades de objeto y proporciona acceso directo a las propiedades del objeto. Para obtener más información, vea [las interfaces iAds y IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md). |
| **IUnknown**         | Se usa para la administración de objetos COM. La interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) es necesaria para todos los objetos com.                                                                                                                                                                                                                                                                              |
| **IDispatch**        | Se usa para la invocación de métodos y datos de la biblioteca de tipos. La interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) es necesaria para todos los objetos de automatización.                                                                                                                                                                                                                             |



 

Los objetos ADSI más complejos pueden exponer interfaces adicionales. Por ejemplo, [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) admite métodos que administran colecciones de elementos de directorio con el mismo tipo de datos. Los métodos de [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) administran las colecciones de casos especiales de los objetos que admiten la interfaz [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) . En el caso de los proveedores que lo admiten, la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) admite métodos para consultar los servicios de directorio. Además, ADSI proporciona interfaces que representan elementos lógicos y físicos conocidos. Por ejemplo, los objetos ADSI que representan a los usuarios admiten [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), los que representan equipos que admiten [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer), etc. Para obtener más información acerca de los objetos ADSI, vea [las interfaces iAds y IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md). No todos los proveedores implementan todas las interfaces o todos los métodos y propiedades de todas las interfaces. Para obtener más información, vea [referencia de ADSI](adsi-reference.md).

 

 